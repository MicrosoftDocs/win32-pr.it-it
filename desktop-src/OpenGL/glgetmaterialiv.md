---
title: Funzione glGetMaterialiv (Gl.h)
description: Le funzioni glGetMaterialfv e glGetMaterialiv restituiscono parametri material. | Funzione glGetMaterialiv (Gl.h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- Funzione glGetMaterialiv OpenGL
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
ms.openlocfilehash: df6babcac908d59c5a5a51b0a23736b760ed25ec542f58339182d3a7536050be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360075"
---
# <a name="glgetmaterialiv-function"></a>Funzione glGetMaterialiv

Le [**funzioni glGetMaterialfv**](glgetmaterialfv.md) e **glGetMaterialiv** restituiscono parametri material.

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

*Faccia* 
</dt> <dd>

Specifica quale dei due materiali viene sottoposto a query. Gl \_ FRONT o GL BACK sono accettati, che rappresentano rispettivamente i materiali anteriore e \_ posteriore.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro material da restituire. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**AMBIENTE \_ GL**</dt> </dl>                    | Il *parametro params* restituisce quattro valori integer o a virgola mobile che rappresentano la riflettenza di ambiente del materiale. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                    | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano la riflessione diffusa del materiale. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_SPECULARE GL**</dt> </dl>                 | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano la riflettenza speculare del materiale. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**EMISSIONE \_ GL**</dt> </dl>                 | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano l'intensità della luce emessa del materiale. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ BRILLANTEZZA**</dt> </dl>              | Il *parametro params* restituisce un intero o un valore a virgola mobile che rappresenta l'esponente speculare del materiale. I valori interi, se richiesti, vengono calcolati arrotondando il valore a virgola mobile interno al valore intero più vicino.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**INDICI \_ DEI \_ COLORI GL**</dt> </dl> | Il *parametro params* restituisce tre valori interi o a virgola mobile che rappresentano gli indici di ambiente, diffusione e speculari del materiale. Usare questi indici solo per l'illuminazione con indici di colore. Gli altri parametri vengono tutti usati solo per l'illuminazione RGBA. I valori interi, se richiesti, vengono calcolati arrotondando i valori a virgola mobile interni ai valori interi più vicini.<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* o *query* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetMaterial** restituisce in *params* il valore o i valori del *parametro pname* del materiale *viso*.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





