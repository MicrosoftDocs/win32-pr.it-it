---
title: funzione glGetMaterialiv (GL. h)
description: Le funzioni glGetMaterialfv e glGetMaterialiv restituiscono parametri di materiale. | funzione glGetMaterialiv (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- funzione glGetMaterialiv OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321419"
---
# <a name="glgetmaterialiv-function"></a>glGetMaterialiv (funzione)

Le funzioni [**glGetMaterialfv**](glgetmaterialfv.md) e **glGetMaterialiv** restituiscono parametri di materiale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*faccia* 
</dt> <dd>

Specifica quale dei due materiali viene sottoposto a query. GL \_ front o GL \_ back sono accettati, che rappresentano rispettivamente i materiali anteriore e posteriore.

</dd> <dt>

*pname* 
</dt> <dd>

Parametro Material da restituire. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                    | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la reflection di ambiente del materiale. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ diffuse**</dt> </dl>                    | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la riflettenza diffusa del materiale. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_speculare GL**</dt> </dl>                 | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la reflection speculare del materiale. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_emissione GL**</dt> </dl>                 | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano l'intensità della luce emessa del materiale. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_lucentezza GL**</dt> </dl>              | Il parametro *params* restituisce un intero o un valore a virgola mobile che rappresenta l'esponente speculare del materiale. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento del valore a virgola mobile interno al valore intero più vicino.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**indici di \_ colore GL \_**</dt> </dl> | Il parametro *params* restituisce tre valori integer o a virgola mobile che rappresentano gli indici di ambiente, diffusi e speculari del materiale. Usare questi indici solo per l'illuminazione degli indici dei colori. Gli altri parametri vengono usati solo per l'illuminazione RGBA. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* o *query* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetMaterial** restituisce in *params* il valore o i valori del parametro *pname* della *superficie* del materiale.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





