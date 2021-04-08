---
title: funzione glFrontFace (GL. h)
description: La funzione glFrontFace definisce i poligoni di fronte e indietro.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- funzione glFrontFace OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964911"
---
# <a name="glfrontface-function"></a>glFrontFace (funzione)

La funzione **glFrontFace** definisce i poligoni di fronte e indietro.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Orientamento dei poligoni in primo piano. GL \_ CW e GL \_ CCW sono accettati. Il valore predefinito è GL \_ CCW.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

In una scena composta interamente da superfici chiuse opache, i poligoni di back-end non sono mai visibili. Eliminando questi poligoni invisibili si ha il vantaggio evidente di velocizzare il rendering dell'immagine. È possibile abilitare e disabilitare l'eliminazione di poligoni di back-end con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) usando la superficie di selezione dell'argomento GL \_ \_ .

La proiezione di un poligono per le coordinate della finestra viene definita in senso orario se un oggetto immaginario che segue il percorso dal primo vertice, il secondo vertice e così via, fino all'ultimo vertice e infine al primo vertice, si sposta in senso orario sull'interno del poligono. La chiusura del poligono viene definita in senso antiorario se l'oggetto immaginario che segue lo stesso percorso si sposta in senso antiorario sull'interno del poligono. La funzione **glFrontFace** specifica se i poligoni con avvolgimento in senso orario nelle coordinate della finestra o in senso antiorario nelle coordinate della finestra vengono portati in primo piano. Passando GL \_ CCW alla *modalità* , vengono selezionati i poligoni in senso antiorario come front-end; GL \_ CW seleziona i poligoni in senso orario come front-end. Per impostazione predefinita, i poligoni in senso antiorario vengono considerati front-end.

La funzione seguente recupera informazioni su **glFrontface**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con front-end GL argomento \_ \_

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





