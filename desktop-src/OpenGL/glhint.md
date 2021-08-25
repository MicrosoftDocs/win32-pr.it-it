---
title: Funzione glHint (Gl.h)
description: La funzione glHint specifica hint specifici dell'implementazione.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- Funzione glHint OpenGL
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
ms.openlocfilehash: 7602b4f0af35c8bc9aeb38cdcb613e30ded907ced75e2241c8ed9e23b57fd98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359647"
---
# <a name="glhint-function"></a>Funzione glHint

La **funzione glHint** specifica hint specifici dell'implementazione.

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
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**SUGGERIMENTO \_ GL \_ OSANNA**</dt> </dl>                                                           | Indica l'accuratezza del calcolo della nebbia. Se il calcolo della nebbia per pixel non è supportato in modo efficiente dall'implementazione OpenGL, l'hintING GL DONT CARE o GL FASTEST può comportare il calcolo per vertice degli effetti \_ \_ della \_ nebbia.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**SUGGERIMENTO \_ DI \_ ARROTONDAMENTO LINEA GL \_**</dt> </dl>                                  | Indica la qualità di campionamento delle linee antialias. Se si applica una funzione di filtro più grande, è possibile che vengano generati più frammenti di pixel durante la \_ rasterizzazione.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**SUGGERIMENTO \_ DI \_ CORREZIONE DELLA PROSPETTIVA GL \_**</dt> </dl> | Indica la qualità dell'interpolazione delle coordinate di colore e trama. Se l'interpolazione dei parametri con correzione della prospettiva non è supportata in modo efficiente dall'implementazione OpenGL, l'hintING GL DONT CARE o GL FASTEST può comportare una semplice interpolazione lineare di colori e/o coordinate di \_ \_ \_ trama.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**SUGGERIMENTO \_ DI \_ ARROTONDAMENTO DEL PUNTO GL \_**</dt> </dl>                               | Indica la qualità di campionamento dei punti antialias. Se si applica una funzione di filtro più grande, è possibile che vengano generati più frammenti di pixel durante la \_ rasterizzazione.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**HINT DI \_ \_ ARROTONDAMENTO POLIGONO GL \_**</dt> </dl>                         | Indica la qualità di campionamento dei poligoni antialias. Se si applica una funzione di filtro più grande, è possibile che vengano generati più frammenti di pixel durante la \_ rasterizzazione.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Costante simbolica che indica il comportamento desiderato. Vengono accettate le costanti simboliche seguenti.



| Valore                                                                                                                                                       | Significato                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ PIÙ VELOCE**</dt> </dl>        | È consigliabile scegliere l'opzione più efficiente.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL \_ NICEST**</dt> </dl>           | È consigliabile scegliere l'opzione più corretta o di massima qualità.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ DONT \_ CARE**</dt> </dl> | Il client non ha una preferenza.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* o *mode* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Quando c'è spazio per l'interpretazione, è possibile controllare determinati aspetti del comportamento di OpenGL con suggerimenti. Specificare un hint con due argomenti. Il *parametro* target è una costante simbolica che indica il comportamento da controllare e *mode* è un'altra costante simbolica che indica il comportamento desiderato.

Anche se gli aspetti di implementazione che possono essere hintati sono ben definiti, l'interpretazione degli hint dipende dall'implementazione.

La **funzione glHint** può essere ignorata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





