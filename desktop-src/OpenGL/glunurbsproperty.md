---
title: Funzione gluNurbsProperty (Glu.h)
description: La funzione gluNurbsProperty imposta una proprietà B-Spline razionale non uniforme (NURBS).
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- Funzione gluNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489031"
---
# <a name="glunurbsproperty-function"></a>Funzione gluNurbsProperty

La **funzione gluNurbsProperty** imposta una proprietà B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Proprietà da impostare. I valori seguenti sono validi:



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**TOLLERANZA \_ DI \_ CAMPIONAMENTO GLU**</dt> </dl>       | Specifica la lunghezza massima, in pixel, da utilizzare quando il metodo di campionamento è impostato su GLU \_ PATH \_ LENGTH. Il valore predefinito è 50,0 pixel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**MODALITÀ \_ DI VISUALIZZAZIONE \_ GLU**</dt> </dl>                         | Il *parametro value* definisce la modalità di rendering di una superficie NURBS. È possibile impostare *value su* GLU \_ FILL, GLU OUTLINE POLYGON o GLU \_ OUTLINE \_ \_ \_ PATCH. <br/> GLU \_ FILL. Il rendering della superficie viene eseguito come set di poligoni. Si tratta del valore predefinito. <br/> POLIGONO \_ GLU \_ OUTLINE. La libreria NURBS disegna solo i contorni dei poligoni creati dalla tessellazione. <br/> PATCH \_ DEL \_ CONTORNO GLU. Vengono tracciati solo i contorni delle patch e delle curve di taglio definite dall'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**GLU \_ CULLING**</dt> </dl>                                         | Il *parametro value* è un valore booleano. Quando il valore è impostato su GL TRUE, le curve NURBS i cui punti di controllo si trovano all'esterno del viewport corrente vengono \_ eliminate prima della tessellazione. Il valore predefinito è GL FALSE perché una curva NURBS non può rientrare completamente nello scafo \_ convesso dei relativi punti di controllo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**MATRICE \_ DI CARICAMENTO AUTOMATICO \_ \_ GLU**</dt> </dl>            | Il *parametro value* è un valore booleano. Se impostato su GL TRUE, il codice NURBS scarica la matrice di proiezione, la matrice modelview e il viewport dal server OpenGL per calcolare le matrici di campionamento ed culling per ogni curva NURBS di cui viene eseguito il \_ rendering. Le matrici di campionamento e di culling sono necessarie per determinare la tessellazione di una superficie NURBS in segmenti di linea o poligoni e per eliminare una superficie NURBS se si trova all'esterno del viewport. <br/> Se questa modalità è impostata su GL FALSE, è necessario fornire una matrice di proiezione, una matrice di visualizzazione del modello e un viewport per il renderer NURBS da usare per costruire matrici di campionamento ed \_ culling. È possibile eseguire questa operazione con la [**funzione gluLoadSamplingMatrices.**](gluloadsamplingmatrices.md)<br/> Il valore predefinito per questa modalità è GL \_ TRUE. La modifica di questa modalità da GL TRUE a GL FALSE non influisce sulle matrici di campionamento e di culling fino a quando non si \_ \_ chiama [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> I parametri di proprietà seguenti sono supportati in GLU versione 1.1 o successiva e non sono validi per GLU versione 1.0: GLU \_ PARAMETRIC \_ TOLERANCE, GLU SAMPLING METHOD, GLU U STEP e \_ GLU V \_ \_ \_ \_ \_ STEP.<br/> I parametri di valore seguenti sono supportati in GLU versione 1.1 o successiva e non sono validi per GLU versione 1.0: GLU \_ PATH \_ LENGTH, GLU PARAMETRIC ERROR e GLU \_ DOMAIN \_ \_ \_ DISTANCE.<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**TOLLERANZA \_ \_ PARAMETRICA GLU**</dt> </dl> | Specifica la distanza massima, in pixel, da utilizzare quando il metodo di campionamento è impostato su GLU \_ PARAMETRIC \_ ERROR. Il valore predefinito è 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**METODO DI \_ \_ CAMPIONAMENTO GLU**</dt> </dl>                | Specifica come eseguire il tessallate di una superficie NURBS. GLU \_ SAMPLING METHOD può avere uno dei tre valori \_ seguenti. <br/> LUNGHEZZA \_ DEL PERCORSO \_ GLU. Il valore predefinito. Specifica che le superfici sottoposte a rendering con la lunghezza massima, in pixel, dei bordi dei poligoni a tessellazione non sono maggiori del valore specificato da GLU \_ SAMPLING \_ TOLERANCE. <br/> ERRORE \_ GLU \_ PARAMETRIC. Specifica che nel rendering della superficie, il valore di GLU PARAMETRIC TOLERANCE specifica la distanza massima, in pixel, tra i poligoni a tessellazione e le superfici \_ \_ approssimative. <br/> GLU \_ DOMAIN \_ DISTANCE. Specifica, in coordinate parametrici, il numero di punti di campionamento per unità di lunghezza da prendere nelle *dimensioni u* *e v.*<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**GLU \_ U \_ STEP**</dt> </dl>                                           | Specifica il numero di punti di campionamento per unità di lunghezza lungo la *dimensione u* in coordinate parametrici. Il valore di GLU \_ U STEP viene usato quando GLU SAMPLING METHOD è impostato su GLU DOMAIN \_ \_ \_ \_ \_ DISTANCE. Il valore predefinito è 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**PASSAGGIO \_ GLU V \_**</dt> </dl>                                           | Specifica il numero di punti di campionamento per unità di lunghezza lungo la *dimensione v* in coordinate parametrici. Il valore di GLU \_ V STEP viene usato quando GLU SAMPLING METHOD è impostato su GLU DOMAIN \_ \_ \_ \_ \_ DISTANCE. Il valore predefinito è 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore su cui impostare la proprietà indicata. Il *parametro value* può essere un valore numerico o uno dei tre valori seguenti: GLU PATH \_ \_ LENGTH, GLU \_ PARAMETRIC ERROR o GLU DOMAIN \_ \_ \_ DISTANCE.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**LUNGHEZZA \_ DEL PERCORSO \_ GLU**</dt> </dl>                | Il valore predefinito. Specifica che le superfici sottoposte a rendering con la lunghezza massima, in pixel, dei bordi dei poligoni a tessellazione non sono maggiori del valore specificato da GLU \_ SAMPLING \_ TOLERANCE.<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**ERRORE \_ GLU \_ PARAMETRIC**</dt> </dl> | Specifica che nel rendering della superficie, il valore di GLU PARAMETRIC TOLERANCE specifica la distanza massima, in pixel, tra i poligoni a tessellazione e le superfici \_ \_ approssimative.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**GLU \_ DOMAIN \_ DISTANCE**</dt> </dl>    | Specifica, in coordinate parametrici, il numero di punti di campionamento per unità di lunghezza da prendere nelle *dimensioni u* *e v.*<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluNurbsProperty** per controllare le proprietà archiviate in un oggetto NURBS. Queste proprietà influiscono sul modo in cui viene eseguito il rendering di una curva NURBS.





 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





