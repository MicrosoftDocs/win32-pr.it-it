---
title: Funzione glColor4sv (Gl.h)
description: Imposta il colore corrente da una matrice già esistente di valori di colore. | Funzione glColor4sv (Gl.h)
ms.assetid: 4fd846b2-b0e7-49ac-988b-0f67537ab0b3
keywords:
- Funzione glColor4sv OpenGL
topic_type:
- apiref
api_name:
- glColor4sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1a35d2286c863c029d059393dfcb581aa9e3563847fed3d160b901a41f8784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061839"
---
# <a name="glcolor4sv-function"></a>Funzione glColor4sv

Imposta il colore corrente da una matrice già esistente di valori di colore.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColor4sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice che contiene i valori rosso, verde, blu e alfa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il gl archivia sia un indice colori a valore singolo corrente che un colore RGBA a quattro valori corrente. **glcolor** imposta un nuovo colore RGBA a quattro valori. **glcolor** ha due varianti principali: **glcolor3** e **glcolor4.** **Le varianti glcolor3** specificano i nuovi valori rosso, verde e blu in modo esplicito e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa). **Le varianti glcolor4** specificano tutti e quattro i componenti di colore in modo esplicito.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i e** **glcolor4i** accettano tre o quattro signed byte, short o long integer come argomenti. Quando v viene aggiunto al nome, i comandi color possono prendere un puntatore a una matrice di tali valori.

I valori dei colori correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa ed esponente non specificati. I componenti di colore di interi senza segno, se specificati, vengono mappati in modo lineare a valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 a 0,0 (intensità zero). Se specificato, i componenti di colore di interi con segno vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. Si noti che questo mapping non converte 0 esattamente in 0.0. I valori a virgola mobile vengono mappati direttamente.

Né i valori a virgola mobile né i valori interi con segno vengono definiti nell'intervallo \[ 0,1 \] prima dell'aggiornamento del colore corrente. Tuttavia, i componenti di colore vengono fissati a questo intervallo prima di essere interpolati o scritti in un buffer dei colori.

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





