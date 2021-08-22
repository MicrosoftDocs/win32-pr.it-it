---
title: Funzione glIndexs (Gl.h)
description: La funzione glIndexs imposta l'indice dei colori corrente.
ms.assetid: 193304e6-c88a-49a6-935b-29bcf1954564
keywords:
- Funzione glIndexs OpenGL
topic_type:
- apiref
api_name:
- glIndexs
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d3e309d8288765e493cac6c586c873d4bb927ca2d0fc89c3b8c621b2e2ed31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493391"
---
# <a name="glindexs-function"></a>Funzione glIndexs

La **funzione glIndexs** imposta l'indice dei colori corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexs(
   GLshort c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*c* 
</dt> <dd>

Nuovo valore per l'indice dei colori corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glIndexs** aggiorna l'indice dei colori corrente (a valore singolo). Accetta un argomento: il nuovo valore per l'indice dei colori corrente.

L'indice corrente viene archiviato come valore a virgola mobile. I valori interi vengono convertiti direttamente in valori a virgola mobile, senza mapping speciale.

I valori di indice non compreso nell'intervallo rappresentabile del index buffer colore non sono ancorati. Tuttavia, prima che un indice venga dithering (se abilitato) e scritto in framebuffer, viene convertito in formato a virgola fissa. Tutti i bit nella parte intera del valore a virgola fissa risultante che non corrispondono ai bit in framebuffer vengono mascherati.

L'indice corrente può essere aggiornato in qualsiasi momento. In particolare, **è possibile chiamare glIndexs** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](glend.md).

La funzione seguente recupera le informazioni correlate a **glIndexs**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ INDEX

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

