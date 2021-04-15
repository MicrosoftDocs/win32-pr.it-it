---
title: funzione gluNurbsProperty (Glu. h)
description: La funzione gluNurbsProperty imposta una proprietà B-spline (NURBS) razionale non uniforme.
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- funzione gluNurbsProperty OpenGL
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
ms.openlocfilehash: 55eb8ed1914f500052c8565f6cc73e56f83bea1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475064"
---
# <a name="glunurbsproperty-function"></a>gluNurbsProperty (funzione)

La funzione **gluNurbsProperty** imposta una proprietà B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.

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

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Proprietà da impostare. I valori seguenti sono validi:



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**\_tolleranza di campionamento Glu \_**</dt> </dl>       | Specifica la lunghezza massima, in pixel, da usare quando il metodo di campionamento è impostato sulla lunghezza del percorso di GLU \_ \_ . Il valore predefinito è 50,0 pixel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**\_modalità di visualizzazione Glu \_**</dt> </dl>                         | Il parametro *value* definisce il modo in cui deve essere eseguito il rendering di una superficie NURBS. È possibile impostare il *valore* su Glu \_ Fill, il \_ poligono del contorno o la patch per il \_ \_ contorno \_ di Glu. <br/> \_riempimento Glu. Viene eseguito il rendering della superficie come un set di poligoni. Si tratta del valore predefinito. <br/> \_poligono del contorno Glu \_ . La libreria NURBS disegna solo i contorni dei poligoni creati dallo schema a mosaico. <br/> \_patch della struttura Glu \_ . Vengono disegnati solo i contorni delle patch e delle curve Trim definite dall'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**eliminazione di GLU \_**</dt> </dl>                                         | Il parametro *value* è un valore booleano. Quando value è impostato su GL \_ true, le curve NURBS i cui punti di controllo si trovano all'esterno del viewport corrente vengono scartate prima dello schema a mosaico. Il valore predefinito è GL \_ false (perché una curva NURBS non può rientrare completamente nella struttura convessa dei punti di controllo).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**\_matrice di \_ caricamento \_ automatico Glu**</dt> </dl>            | Il parametro *value* è un valore booleano. Se impostato su GL \_ true, il codice NURBS Scarica la matrice di proiezione, la matrice Modelview e il viewport dal server OpenGL per calcolare le matrici di campionamento ed eliminazione per ogni curva NURBS di cui viene eseguito il rendering. Le matrici di campionamento ed eliminazione sono necessarie per determinare lo schema a mosaico di una superficie NURBS in segmenti di linea o poligoni e per eliminare una superficie NURBS se si trova all'esterno del viewport. <br/> Se questa modalità è impostata su GL \_ false, è necessario fornire una matrice di proiezione, una matrice Modelview e un viewport per il RENDERER NURBS da usare per costruire matrici di campionamento e di eliminazione. Questa operazione può essere eseguita con la funzione [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md) .<br/> Il valore predefinito per questa modalità è GL \_ true. La modifica di questa modalità da GL \_ true a GL \_ false non influisce sulle matrici di campionamento e di eliminazione fino a quando non si chiama [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> I parametri di proprietà seguenti sono supportati nella versione GLU 1,1 o versioni successive e non sono validi per GLU versione 1,0: la \_ tolleranza PARAmetrica Glu \_ , il metodo di \_ campionamento Glu, il \_ \_ passaggio GLU U e il \_ \_ passaggio Glu V \_ .<br/> I parametri di valore seguenti sono supportati nella versione GLU 1,1 o versioni successive e non sono validi per GLU versione 1,0: lunghezza del percorso di Glu \_ \_ , Glu \_ parametrico \_ Error e Glu \_ Domain \_ distance.<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**\_tolleranza PARAmetrica Glu \_**</dt> </dl> | Specifica la distanza massima, in pixel, da usare quando il metodo di campionamento è impostato su GLU \_ PARAmetrico \_ Error. Il valore predefinito è 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**\_metodo di campionamento Glu \_**</dt> </dl>                | Specifica come tessallate una superficie NURBS. \_ \_ Il metodo di campionamento Glu può avere uno dei tre valori seguenti. <br/> lunghezza del percorso di GLU \_ \_ . Il valore predefinito. Specifica che le superfici sottoposte a rendering con la lunghezza massima, in pixel, dei bordi dei poligoni a mosaico non sono maggiori del valore specificato dalla \_ tolleranza di campionamento Glu \_ . <br/> \_errore PARAmetrico Glu \_ . Specifica che, durante il rendering della superficie, il valore della \_ tolleranza PARAmetrica Glu \_ specifica la distanza massima, in pixel, tra i poligoni a mosaico e le superfici che approssimano. <br/> \_distanza del dominio Glu \_ . Specifica, in coordinate parametriche, il numero di punti campione per lunghezza unità da eseguire nelle dimensioni *u* e *v* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**GLU \_ U \_ Step**</dt> </dl>                                           | Specifica il numero di punti di campionamento per lunghezza di unità effettuate lungo la dimensione *u* nelle coordinate parametriche. Il valore di GLU \_ U \_ Step viene usato quando il \_ metodo di campionamento Glu \_ è impostato su Glu \_ Domain \_ distance. Il valore predefinito è 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**passaggio di GLU \_ V \_**</dt> </dl>                                           | Specifica il numero di punti di esempio per lunghezza di unità effettuate lungo la dimensione *v* nelle coordinate parametriche. Il valore del passaggio di GLU \_ V \_ viene usato quando il \_ metodo di campionamento Glu \_ è impostato su Glu \_ Domain \_ distance. Il valore predefinito è 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore in cui impostare la proprietà indicata. Il parametro del *valore* può essere un valore numerico o uno dei tre valori seguenti: lunghezza del percorso di Glu \_ \_ , \_ errore parametrico di GLU \_ o \_ distanza del dominio Glu \_ .



| Valore                                                                                                                                                                               | Significato                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**\_Lunghezza percorso \_ Glu**</dt> </dl>                | Il valore predefinito. Specifica che le superfici sottoposte a rendering con la lunghezza massima, in pixel, dei bordi dei poligoni a mosaico non sono maggiori del valore specificato dalla \_ tolleranza di campionamento Glu \_ .<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**\_errore di PARAmetrizzazione Glu \_**</dt> </dl> | Specifica che, durante il rendering della superficie, il valore della \_ tolleranza PARAmetrica Glu \_ specifica la distanza massima, in pixel, tra i poligoni a mosaico e le superfici che approssimano.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**\_distanza del dominio Glu \_**</dt> </dl>    | Specifica, in coordinate parametriche, il numero di punti campione per lunghezza unità da eseguire nelle dimensioni *u* e *v* .<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluNurbsProperty** per controllare le proprietà archiviate in un oggetto NURBS. Queste proprietà influiscono sul modo in cui viene eseguito il rendering di una curva NURBS.





 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





