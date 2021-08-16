---
title: Funzione glMateriali (Gl.h)
description: La funzioneglMateriali specifica i parametri dei materiali per il modello di illuminazione.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- Funzione glMateriali OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d850bac6b27672c00dca9b1cafa7b4664dbde5fca0085381b4b166e2106b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358865"
---
# <a name="glmateriali-function"></a>Funzione glMateriali

La **funzione glMateriali** specifica i parametri dei materiali per il modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Faccia* 
</dt> <dd>

Viso o visi da aggiornare. Deve essere uno dei seguenti: GL \_ FRONT, GL \_ BACK o GL FRONT e GL \_ \_ BACK.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro materiale a valore singolo del viso o dei visi da aggiornare. Deve essere \_ GL- ERRETÀ.



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ SHININESS**</dt> </dl> | Il *parametro param* è un singolo numero intero che specifica l'esponente speculare RGBA del materiale. I valori interi vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] L'esponente speculare predefinito per i materiali anteriore e posteriore è 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore sul quale verrà impostato il parametro \_ GL GL GLINESS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>  | Viso *o* *pname non* è un valore accettato.<br/>                |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | È stato specificato un esponente speculare non compreso \[ nell'intervallo 0, 128. \]<br/> |



## <a name="remarks"></a>Commenti

La **funzione glMateriali** assegna valori ai parametri material. Esistono due set corrispondenti di parametri di materiale. Uno, il *set* anteriore, viene usato per ombreggiatura di punti, linee, bitmap e tutti i poligoni (quando l'illuminazione a due lati è disabilitata) o solo per i poligoni frontali (quando è abilitata l'illuminazione fronte-lato). L'altro set, *rivolto all'indietro,* viene usato per ombreggiaturare i poligoni rivolti all'indietro solo quando è abilitata l'illuminazione a due lati. Fare riferimento [**a glLightModel**](gllightmodel-functions.md) per informazioni dettagliate sui calcoli dell'illuminazione su un lato e su due lati.

La **funzione glMateriali** accetta tre argomenti. Il primo, *viso,* specifica se i materiali GL FRONT, GL BACK o entrambi i materiali \_ GL FRONT e BACK verranno \_ \_ \_ \_ modificati. Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verrà modificato. Il terzo, *param*, specifica il valore che verrà assegnato al parametro specificato.

I parametri dei materiali vengono usati nell'equazione di illuminazione che viene facoltativamente applicata a ogni vertice. L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).

I parametri del materiale possono essere aggiornati in qualsiasi momento. In particolare, **glMateriali** può essere chiamato tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Se è necessario modificare un solo parametro material per vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto **a glMateriali**.

La funzione seguente recupera le informazioni correlate a **glMateriali:**

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





