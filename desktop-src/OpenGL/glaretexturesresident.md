---
title: Funzione glAreTexturesResident (Gl.h)
description: La funzione glAreTexturesResident determina se gli oggetti trama specificati sono residenti nella memoria della trama.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- Funzione glAreTexturesResident OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c503cac59bbec912c535120161d27991118dab818a185c1f39d8f48cb2a5939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082241"
---
# <a name="glaretexturesresident-function"></a>Funzione glAreTexturesResident

La **funzione glAreTexturesResident** determina se gli oggetti trama specificati sono residenti nella memoria della trama.

## <a name="syntax"></a>Sintassi


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero di trame su cui eseguire query.

</dd> <dt>

*Texture* 
</dt> <dd>

Indirizzo di una matrice contenente i nomi delle trame su cui eseguire la query.

</dd> <dt>

*Residence* 
</dt> <dd>

Indirizzo di una matrice in cui viene restituito lo stato della trama. Lo stato di residenza di una trama denominata da un elemento *di trame* viene restituito nell'elemento corrispondente di *.*

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *n* è un valore negativo, un elemento nelle *trame* è zero o un elemento nelle *trame* non contiene un identificatore di trama.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Commenti

Nei computer con una quantità limitata di memoria della trama, OpenGL stabilisce un working set di trame residenti nella memoria delle trame. Queste trame possono essere associate a una destinazione di trama in modo molto più efficiente rispetto alle trame che non sono residenti.

La **funzione glAreTexturesResident** esegue una query sullo stato di trama delle *n* trame denominate dagli elementi *delle trame*. Se tutte le trame denominate sono residenti, **glAreTexturesResident** restituisce GL TRUE e il contenuto delle trame non è \_ indisturbato.  Se una delle trame denominate non è residenti, **glAreTexturesResident** restituisce GL FALSE e lo stato dettagliato viene restituito negli \_ *elementi n* di *.*

Se un elemento di *è* GL TRUE, la trama denominata dall'elemento corrispondente delle \_ *trame* risiede nella memoria della trama.

Per eseguire una query sullo stato di sincronizzazione di  una singola trama associata, chiamare [**glGetTexParameter**](glgettexparameter.md) con il parametro di destinazione impostato sulla trama di destinazione a cui è associata la destinazione e impostare il *parametro pname* su GL \_ TEXTURE \_ RESIDENT. È necessario usare questo metodo per eseguire una query sullo stato residenti di una trama predefinita.

Non è possibile **includere glAreTexturesResident negli** elenchi visualizzati.

La **funzione glAreTexturesResident** restituisce lo stato di residenza delle trame al momento della chiamata. Non garantisce che le trame rimangano residenti in qualsiasi altro momento.

Se le trame risiedono nella memoria virtuale (non è presente alcuna memoria di trama), vengono considerate sempre residenti.

> [!Note]  
> La **funzione glAreTexturesResident** è disponibile solo in OpenGL versione 1.1 o successiva.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





