FIND_PACKAGE( CityGML )
IF(CITYGML_FOUND)
	INCLUDE_DIRECTORIES( ${OSG_INCLUDE_DIRS} ${CITYGML_INCLUDE_DIR} )

	SET( TARGET_SRC ReaderWriterCityGML.cpp )

	SET( TARGET_ADDED_LIBRARIES osgText )
	SET( TARGET_LIBRARIES_VARS CITYGML_LIBRARY XERCESC_LIBRARY LIBXML2_LIBRARY OPENGL_glu_LIBRARY )

	SETUP_PLUGIN( citygml )
ENDIF()
