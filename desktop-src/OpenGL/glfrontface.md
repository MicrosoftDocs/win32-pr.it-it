---
title: Funzione glFrontFace (Gl.h)
description: La funzione glFrontFace definisce poligoni anteriore e posteriore.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- Funzione glFrontFace OpenGL
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
ms.openlocfilehash: 91d288b4e6380ab845af9a05381963444e28ddf50739ecd3f5563d9f2dc729fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580161"
---
# <a name="glfrontface-function"></a>Funzione glFrontFace

La **funzione glFrontFace** definisce poligoni anteriore e posteriore.

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

Orientamento dei poligoni rivolti anteriore. Sono accettati GL \_ CW \_ e GL CCW. Il valore predefinito è GL \_ CCW.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *mode* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

In una scena composta interamente da superfici chiuse opache, i poligoni rivolti all'indietro non sono mai visibili. L'eliminazione di questi poligoni invisibili ha l'ovvio vantaggio di velocizzare il rendering dell'immagine. È possibile abilitare e disabilitare l'eliminazione di poligoni rivolti all'indietro con [**glEnable**](glenable.md) [**e glDisable**](gldisable.md) usando l'argomento GL \_ CULL \_ FACE.

Si dice che la proiezione di un poligono alle coordinate della finestra abbia un avvolgimento in senso orario se un oggetto immaginario che segue il percorso dal primo vertice, dal secondo vertice e così via all'ultimo vertice e infine di nuovo al primo vertice, si sposta in senso orario verso l'interno del poligono. Il vento del poligono si dice in senso antiorario se l'oggetto immaginario che segue lo stesso percorso si sposta in senso antiorario verso l'interno del poligono. La **funzione glFrontFace** specifica se i poligoni con avvolgimento in senso orario nelle coordinate della finestra o in senso antiorario nelle coordinate della finestra devono essere rivolti anteriore. Il passaggio del CCW GL alla modalità seleziona i poligoni in senso \_ antiorario come  frontali; GL \_ CW seleziona i poligoni in senso orario come anteriore. Per impostazione predefinita, i poligoni in senso antiorario vengono presi in primo piano.

La funzione seguente recupera informazioni su **glFrontface:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ FRONT \_ FACE

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





