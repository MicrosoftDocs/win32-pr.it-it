---
title: Funzione glColor4s (Gl.h)
description: Imposta il colore corrente. | Funzione glColor4s (Gl.h)
ms.assetid: a942e308-8507-4afe-8941-2b9c7e39bb3d
keywords:
- Funzione glColor4s OpenGL
topic_type:
- apiref
api_name:
- glColor4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240c99cb70b27b7112ac7eaa6c1db7175d1aef38f3f510a047a429ffc394268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675601"
---
# <a name="glcolor4s-function"></a>Funzione glColor4s

Imposta il colore corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColor4s(
   GLshort red,
   GLshort green,
   GLshort blue,
   GLshort alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Rosso* 
</dt> <dd>

Nuovo valore rosso per il colore corrente.

</dd> <dt>

*Verde* 
</dt> <dd>

Nuovo valore verde per il colore corrente.

</dd> <dt>

*Blu* 
</dt> <dd>

Nuovo valore blu per il colore corrente.

</dd> <dt>

*Alfa* 
</dt> <dd>

Nuovo valore alfa per il colore corrente.

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

 

 





