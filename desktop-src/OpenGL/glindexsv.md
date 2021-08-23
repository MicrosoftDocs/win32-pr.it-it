---
title: Funzione glIndexsv (Gl.h)
description: La funzione glIndexsv imposta l'indice dei colori corrente.
ms.assetid: 4b7f4edf-a7c8-4e81-8448-5181295d5174
keywords:
- Funzione glIndexsv OpenGL
topic_type:
- apiref
api_name:
- glIndexsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31bbc81da47f9dc0ac17e003d3c27b8882855dc487200c4791e33e21bad4fb62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012139"
---
# <a name="glindexsv-function"></a>Funzione glIndexsv

La **funzione glIndexsv** imposta l'indice dei colori corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexsv(
   const GLshort *c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*c* 
</dt> <dd>

Puntatore a una matrice a un elemento che contiene il nuovo valore per l'indice colori corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glIndexsv** aggiorna l'indice dei colori corrente (a valore singolo). Accetta un argomento: il nuovo valore per l'indice colori corrente.

L'indice corrente viene archiviato come valore a virgola mobile. I valori interi vengono convertiti direttamente in valori a virgola mobile, senza mapping speciale.

I valori di indice esterni all'intervallo rappresentabile del colore index buffer non sono ancorati. Tuttavia, prima che un indice venga dithering (se abilitato) e scritto nel framebuffer, viene convertito in formato a virgola fissa. Tutti i bit nella parte intera del valore a virgola fissa risultante che non corrispondono ai bit nel framebuffer vengono mascherati.

L'indice corrente può essere aggiornato in qualsiasi momento. In particolare, **glIndexsv** può essere chiamato tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](glend.md).

La funzione seguente recupera le informazioni correlate a **glIndexsv**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT \_ INDEX

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

 

