---
title: Funzione glPopClientAttrib (Gl.h)
description: Le funzioni glPushClientAttrib e glPopClientAttrib salvano e ripristinano gruppi di variabili di stato client nello stack di attributi client. | Funzione glPopClientAttrib (Gl.h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- Funzione glPopClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488b689c72f64e20be6871dc95497ac08ce3e0fe45c6ae59471fed0ec0e427b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980793"
---
# <a name="glpopclientattrib-function"></a>Funzione glPopClientAttrib

Le [**funzioni glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** salvano e ripristinano gruppi di variabili di stato client nello stack di attributi client.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                               | Significato                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl> | La funzione è stata chiamata mentre lo stack dell'attributo client era pieno.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPushClientAttrib** usa il relativo parametro mask per determinare quali gruppi di variabili di stato client vengono salvati nello stack dell'attributo client. È possibile usare l'operatore OR bit per bit per unire le costanti simboliche accettate per impostare i bit e costruire una maschera.

La **funzione glPopClientAttrib** ripristina i valori delle variabili di stato client salvate per l'ultima volta con **glPushclientAttrib**. Le variabili di stato client non salvate in precedenza rimangono invariate. Il push degli attributi in uno stack completo di attributi client o l'es estratto di attributi da uno stack vuoto imposta un flag di errore e non vengono apportate altre modifiche allo stato OpenGL. Per impostazione predefinita, lo stack di attributi client è vuoto.

Alcuni valori dello stato client OpenGL non possono essere salvati nello stack di attributi client. Ad esempio, non è possibile salvare gli stati di selezione o feedback nello stack di attributi client. La profondità dello stack dell'attributo client è almeno 16.

Le **funzioni glPushclientAttrib** e **glPopClientAttrib** non vengono compilate in elenchi di visualizzazione, ma vengono eseguite immediatamente.

Le **funzioni glPushClientAttrib** e **glPopClientAttrib** possono solo eseguire il push e il pop delle modalità di archiviazione pixel e degli stati client dell'array di vertici. È necessario usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per eseguire il push e il pop degli stati mantenuti nel server.

> [!Note]  
> Le **funzioni glPushClientAttrib** **e glPopClientAttrib** sono disponibili solo in OpenGL versione 1.1 o successiva.

 

Le funzioni seguenti recuperano informazioni correlate **a glPushClientAttrib** e **glPopClientAttrib:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CLIENT \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAX \_ CLIENT \_ ATTRIB STACK \_ \_ DEPTH

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





