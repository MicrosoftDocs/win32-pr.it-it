---
title: Funzione glIndexf (Gl.h)
description: La funzione glIndexf imposta l'indice dei colori corrente.
ms.assetid: 1109c6b0-daf6-4b93-8e9e-5dd542b6f7c8
keywords:
- Funzione glIndexf OpenGL
topic_type:
- apiref
api_name:
- glIndexf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb53fa34ff3723fc8539f547627b985ea2884b0dffd7d83a431e26acb25a2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359529"
---
# <a name="glindexf-function"></a>Funzione glIndexf

La **funzione glIndexf** imposta l'indice dei colori corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexf(
   GLfloat c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*c* 
</dt> <dd>

Nuovo valore per l'indice colori corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glIndexf** aggiorna l'indice dei colori corrente (a valore singolo). Accetta un argomento: il nuovo valore per l'indice colori corrente.

L'indice corrente viene archiviato come valore a virgola mobile. I valori interi vengono convertiti direttamente in valori a virgola mobile, senza mapping speciale.

I valori di indice esterni all'intervallo rappresentabile del colore index buffer non sono ancorati. Tuttavia, prima che un indice venga dithering (se abilitato) e scritto nel framebuffer, viene convertito in formato a virgola fissa. Tutti i bit nella parte intera del valore a virgola fissa risultante che non corrispondono ai bit nel framebuffer vengono mascherati.

L'indice corrente può essere aggiornato in qualsiasi momento. In particolare, **glIndexf** può essere chiamato tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](glend.md).

La funzione seguente recupera le informazioni correlate a **glIndexf**:

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

 

