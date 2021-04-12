---
title: funzione glHint (GL. h)
description: La funzione glHint specifica hint specifici dell'implementazione.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- funzione glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119303"
---
# <a name="glhint-function"></a>glHint (funzione)

La funzione **glHint** specifica hint specifici dell'implementazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Costante simbolica che indica il comportamento da controllare. Vengono accettate le costanti simboliche seguenti, insieme alla semantica suggerita.



| Valore                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**\_hint di nebbia GL \_**</dt> </dl>                                                           | Indica l'accuratezza del calcolo di nebbia. Se il calcolo della nebbia per pixel non è supportato in modo efficiente dall'implementazione di OpenGL, l'hinting GL \_ dont \_ care o GL più \_ veloci possono determinare un calcolo per vertice degli effetti di nebbia.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**\_ \_ hint uniforme linea \_ GL**</dt> </dl>                                  | Indica la qualità di campionamento delle linee con antialias. L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**HINT per la \_ correzione della prospettiva GL \_ \_**</dt> </dl> | Indica la qualità del colore e l'interpolazione delle coordinate di trama. Se l'interpolazione dei parametri con correzione della prospettiva non è supportata in modo efficiente dall'implementazione di OpenGL, l'hinting GL \_ dont \_ care o GL \_ più veloci possono produrre un'interpolazione lineare semplice di colori e/o coordinate di trama.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**\_ \_ Suggerimento smussato del punto GL \_**</dt> </dl>                               | Indica la qualità di campionamento dei punti antialias. L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**\_hint Smooth poligono GL \_ \_**</dt> </dl>                         | Indica la qualità di campionamento dei poligoni con antialias. L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Costante simbolica che indica il comportamento desiderato. Vengono accettate le seguenti costanti simboliche.



| Valore                                                                                                                                                       | Significato                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**CONTABILITÀ più \_ veloce**</dt> </dl>        | È consigliabile scegliere l'opzione più efficiente.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL più \_ bello**</dt> </dl>           | È consigliabile scegliere l'opzione più corretta, o di qualità più elevata.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ dont \_ care**</dt> </dl> | Il client non ha preferenze.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione* o la *modalità* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Quando è disponibile spazio per l'interpretazione, è possibile controllare alcuni aspetti del comportamento di OpenGL con hint. È possibile specificare un hint con due argomenti. Il parametro di *destinazione* è una costante simbolica che indica il comportamento da controllare e la *modalità* è un'altra costante simbolica che indica il comportamento desiderato.

Sebbene gli aspetti di implementazione che è possibile suggerire siano ben definiti, l'interpretazione degli hint dipende dall'implementazione di.

La funzione **glHint** può essere ignorata.

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

[**Remo**](glend.md)
</dt> </dl>

 

 





