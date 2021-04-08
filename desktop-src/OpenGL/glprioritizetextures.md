---
title: funzione glPrioritizeTextures (GL. h)
description: La funzione glPrioritizeTextures imposta la priorità di residenza delle trame.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- funzione glPrioritizeTextures OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740647"
---
# <a name="glprioritizetextures-function"></a>glPrioritizeTextures (funzione)

La funzione **glPrioritizeTextures** imposta la priorità di residenza delle trame.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero di trame da assegnare in ordine di priorità.

</dd> <dt>

*trame* 
</dt> <dd>

Puntatore al primo elemento di una matrice contenente i nomi delle trame da assegnare in ordine di priorità.

</dd> <dt>

*priorità* 
</dt> <dd>

Puntatore al primo elemento di una matrice contenente le priorità della trama. Una priorità specificata in un elemento *del parametro* prioritys viene applicata alla trama denominata dall'elemento corrispondente del parametro *Textures* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *n* è un valore negativo.<br/>                                                                                                  |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPrioritizeTextures** assegna le priorità di trama *n* specificate nel parametro *priorità* alle *n* trame denominate nel parametro *Textures* . Nei computer con una quantità limitata di memoria di trama, OpenGL stabilisce un "working set" di trame che sono residenti nella memoria della trama. Queste trame possono essere associate a una destinazione di trama in modo molto più efficiente rispetto alle trame non residenti.

Specificando una priorità per ogni trama, la funzione **glPrioritizeTextures** consente di determinare quali trame devono essere residenti.

Gli elementi priorità trama nelle *priorità* vengono fissati nell'intervallo \[ 0,0, 1,0 \] prima di essere assegnati. Zero indica la priorità più bassa; in questo modo, le trame con priorità zero sono meno idonee per la residenza. Il valore 1,0 indica la priorità più alta. in questo modo, è probabile che le trame con priorità 1,0 siano residenti. Tuttavia, non è garantito che le trame siano residenti fino a quando non sono associate.

La funzione **glPrioritizeTextures** ignora i tentativi di assegnazione delle priorità alla trama 0 o a qualsiasi nome di trama che non corrisponde a una trama esistente. Nessuna delle funzioni denominate dal parametro *Textures* deve essere associata a una destinazione di trama.

Se una trama è attualmente associata, è anche possibile usare la funzione [**glTexParameter**](gltexparameter-functions.md) per impostarne la priorità. Questo è l'unico modo per impostare la priorità di una trama predefinita.

È possibile includere **glPrioritizeTextures** negli elenchi di visualizzazione.

La funzione seguente recupera la priorità di una trama attualmente associata a **glPrioritizeTextures**:

-   [**glGetTexParameter**](glgettexparameter.md) con nome parametro \_ priorità trama \_ GL

> [!Note]  
> La funzione **glPrioritizeTextures** è disponibile solo in OpenGL versione 1,1 o successiva.

 

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





