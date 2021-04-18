---
title: funzione glIndexiv (GL. h)
description: La funzione glIndexiv imposta l'indice dei colori corrente.
ms.assetid: 642c243f-046d-474e-8075-ef5692797020
keywords:
- funzione glIndexiv OpenGL
topic_type:
- apiref
api_name:
- glIndexiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf4a4f4bb798a1a93e9d3e31c66b9245a868afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301261"
---
# <a name="glindexiv-function"></a>glIndexiv (funzione)

La funzione **glIndexiv** imposta l'indice dei colori corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexiv(
   const GLint *c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*c* 
</dt> <dd>

Puntatore a una matrice a un elemento che contiene il nuovo valore per l'indice dei colori corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glIndexiv** aggiorna l'indice dei colori corrente (a valore singolo). Accetta un solo argomento: il nuovo valore per l'indice dei colori corrente.

L'indice corrente viene archiviato come valore a virgola mobile. I valori integer vengono convertiti direttamente in valori a virgola mobile, senza mapping speciale.

I valori di indice al di fuori dell'intervallo rappresentabile del buffer dell'indice colori non vengono bloccati. Tuttavia, prima che un indice sia reindirizzato (se abilitato) e scritto nel framebuffer, viene convertito nel formato a virgola fissa. Eventuali bit nella parte intera del valore a virgola fissa risultante che non corrispondono a BITS nel framebuffer vengono mascherati.

L'indice corrente può essere aggiornato in qualsiasi momento. In particolare, è possibile chiamare **glIndexiv** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](glend.md).

La funzione seguente recupera le informazioni correlate a **glIndexiv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ index

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

