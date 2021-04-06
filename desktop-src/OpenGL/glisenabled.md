---
title: funzione glIsEnabled (GL. h)
description: La funzione gllsEnabled verifica se una funzionalità è abilitata.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- funzione glIsEnabled OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdb2ba206e0a026aef118b06d66097ade9ba9ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743127"
---
# <a name="glisenabled-function"></a>glIsEnabled (funzione)

La funzione **gllsEnabled** verifica se una funzionalità è abilitata.

## <a name="syntax"></a>Sintassi


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*limite* 
</dt> <dd>

Costante simbolica che indica una funzionalità OpenGL. Sono accettate le funzionalità seguenti.



| Valore                                                                                                                                                                                                    | Significato                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**\_test GL Alpha \_**</dt> </dl>                                           | Vedere [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**GL \_ auto \_ normale**</dt> </dl>                                        | Vedere [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**\_Blend GL**</dt> </dl>                                                           | Vedere [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * GL \_ clip \_ plane * i * * *</dt> </dl> | Vedere [ **glClipPlane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_matrice di colori GL \_**</dt> </dl>                                        | Vedere [ **glColorPointer**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**\_operazione di \_ logica \_ colori GL**</dt> </dl>                              | Vedere [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**\_materiale colore \_ GL**</dt> </dl>                               | Vedere [ **glColorMaterial**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**superficie di selezione GL \_ \_**</dt> </dl>                                              | Vedere [ **glCullFace**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**\_test di profondità GL \_**</dt> </dl>                                           | Vedere [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**\_dithering GL**</dt> </dl>                                                        | Vedere [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**\_nebbia GL**</dt> </dl>                                                                 | Vedere [ **glFog**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_matrice di indici GL \_**</dt> </dl>                                        | Vedere [ **glIndexPointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**\_ \_ operazione logica indice \_ GL**</dt> </dl>                              | Vedere [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * GL \_ Light * i * * *</dt> </dl>                      | Vedere [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**\_illuminazione GL**</dt> </dl>                                                  | Vedere [**glMaterial**](glmaterial-functions.md), [**glLightModel**](gllightmodel-functions.md)e [**glLight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**\_linea GL \_ smussata**</dt> </dl>                                        | Vedere [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**\_stipple linea \_ GL**</dt> </dl>                                     | Vedere [ **glLineStipple**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**\_Mappa1 \_ colore \_ 4 GL**</dt> </dl>                                    | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Indice MAPPA1 \_ GL**</dt> </dl>                                           | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**\_Normale MAPPA1 \_ GL**</dt> </dl>                                        | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 1**</dt> </dl>           | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**\_ \_ Coord trama GL \_ Mappa1 \_ 2**</dt> </dl>           | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 3**</dt> </dl>           | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 4**</dt> </dl>           | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**\_Vertice GL \_ Mappa1 \_ 3**</dt> </dl>                                 | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**\_Mappa1 \_ Vertex \_ 4**</dt> </dl>                                 | Vedere [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**\_Map2 \_ colore \_ 4 GL**</dt> </dl>                                    | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**\_Indice map2 \_ GL**</dt> </dl>                                           | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**\_Normale map2 \_ GL**</dt> </dl>                                        | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 1**</dt> </dl>           | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**\_ \_ Coord trama GL \_ map2 \_ 2**</dt> </dl>           | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 3**</dt> </dl>           | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 4**</dt> </dl>           | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**\_Vertice GL \_ map2 \_ 3**</dt> </dl>                                 | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**\_Map2 \_ Vertex \_ 4**</dt> </dl>                                 | Vedere [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_matrice normale \_ GL**</dt> </dl>                                     | Vedere [ **glNormalPointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**\_normalizzare GL**</dt> </dl>                                               | Vedere [ **glNormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**\_punto GL \_ smussato**</dt> </dl>                                     | Vedere [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**\_riempimento offset poligono GL \_ \_**</dt> </dl>               | Vedere [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**\_linea offset poligono GL \_ \_**</dt> </dl>               | Vedere [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**\_punto di offset del poligono GL \_ \_**</dt> </dl>            | Vedere [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**\_poligono GL \_ smussato**</dt> </dl>                               | Vedere [ **glPolygonMode**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**\_stipple poligono GL \_**</dt> </dl>                            | Vedere [ **glPolygonStipple**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**\_test della forbice GL \_**</dt> </dl>                                     | Vedere [ **glScissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**\_test stencil \_ GL**</dt> </dl>                                     | Vedere [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**\_Trama GL \_ 1D**</dt> </dl>                                           | Vedere [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**\_Trama GL \_ 2D**</dt> </dl>                                           | Vedere [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_ \_ matrice Coord trama \_ GL**</dt> </dl>               | Vedere [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**\_generazione trama \_ GL \_ Q**</dt> </dl>                                 | Vedere [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**\_generazione trama \_ GL \_ R**</dt> </dl>                                 | Vedere [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**\_generazione trama \_ GL \_**</dt> </dl>                                 | Vedere [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**\_gen trama \_ GL \_ T**</dt> </dl>                                 | Vedere [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_matrice di vertici GL \_**</dt> </dl>                                     | Vedere [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *limite* non è un valore accettato.<br/>                                                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **gllsEnabled** restituisce GL \_ true se *Cap* è una funzionalità abilitata e restituisce GL \_ false in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> </dl>

 

 





