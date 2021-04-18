---
title: funzione glAreTexturesResident (GL. h)
description: La funzione glAreTexturesResident determina se gli oggetti di trama specificati sono residenti nella memoria della trama.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- funzione glAreTexturesResident OpenGL
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
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301805"
---
# <a name="glaretexturesresident-function"></a>glAreTexturesResident (funzione)

La funzione **glAreTexturesResident** determina se gli oggetti di trama specificati sono residenti nella memoria della trama.

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

Numero di trame su cui eseguire la query.

</dd> <dt>

*trame* 
</dt> <dd>

Indirizzo di una matrice contenente i nomi delle trame su cui eseguire la query.

</dd> <dt>

*Residenze* 
</dt> <dd>

Indirizzo di una matrice in cui viene restituito lo stato della residenza della trama. Lo stato di residenza di una trama denominata da un elemento di *trame* viene restituito nell'elemento corrispondente di *Residences*.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *n* è un valore negativo, un elemento nelle *trame* è zero oppure un elemento nelle *trame* non contiene un identificatore di trama.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Commenti

Nei computer con una quantità limitata di memoria di trama, OpenGL stabilisce un working set di trame che sono residenti nella memoria della trama. Queste trame possono essere associate a una destinazione di trama in modo molto più efficiente rispetto alle trame non residenti.

La funzione **glAreTexturesResident** esegue una query sullo stato di residenza della trama delle trame *n* denominate dagli elementi delle *trame*. Se tutte le trame denominate sono residenti, **glAreTexturesResident** restituisce GL \_ true e il contenuto delle *residenze* non viene disturbato. Se una delle trame denominate non è residente, **glAreTexturesResident** restituisce GL \_ false e viene restituito lo stato dettagliato negli *n* elementi di *Residences*.

Se un elemento di *Residences* è GL \_ true, la trama denominata dall'elemento corrispondente delle *trame* sarà residente nella memoria della trama.

Per eseguire una query sullo stato di residenza di una singola trama con binding, chiamare [**glGetTexParameter**](glgettexparameter.md) con il parametro di *destinazione* impostato sulla trama di destinazione a cui è associata la destinazione e impostare il parametro *pname* su GL \_ texture \_ Resident. È necessario utilizzare questo metodo per eseguire una query sullo stato residente di una trama predefinita.

Non è possibile includere **glAreTexturesResident** negli elenchi di visualizzazione.

La funzione **glAreTexturesResident** restituisce lo stato di residenza delle trame al momento della chiamata. Non garantisce che le trame rimangano residenti in qualsiasi altro momento.

Se le trame risiedono nella memoria virtuale (non è presente alcuna memoria di trama), vengono considerate sempre residenti.

> [!Note]  
> La funzione **glAreTexturesResident** è disponibile solo in OpenGL versione 1,1 o successiva.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





