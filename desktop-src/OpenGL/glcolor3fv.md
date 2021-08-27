---
title: Funzione glColor3fv (Gl.h)
description: Imposta il colore corrente da una matrice già esistente di valori di colore. | Funzione glColor3fv (Gl.h)
ms.assetid: 4ffaaa7e-4fa3-45b8-acf0-850e1e9d9a60
keywords:
- Funzione glColor3fv OpenGL
topic_type:
- apiref
api_name:
- glColor3fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533256054c847d01b0e4799f58736b49fbad2aff399452bdcb2d956c8ee610fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081911"
---
# <a name="glcolor3fv-function"></a>Funzione glColor3fv

Imposta il colore corrente da una matrice già esistente di valori di colore.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColor3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice che contiene valori rosso, verde e blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Gl archivia sia un indice colori a valore singolo corrente che un colore RGBA a quattro valori corrente. **glcolor** imposta un nuovo colore RGBA a quattro valori. **glcolor** ha due varianti principali: **glcolor3** e **glcolor4**. **Le varianti glcolor3** specificano in modo esplicito i nuovi valori rosso, verde e blu e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa). **Le varianti glcolor4** specificano in modo esplicito tutti e quattro i componenti di colore.

**glcolor3b,** **glcolor4b,** **glcolor3s,** **glcolor4s,** **glcolor3i** e **glcolor4i** accettano tre o quattro interi con segno, short o long come argomenti. Quando v viene aggiunto al nome, i comandi color possono prendere un puntatore a una matrice di tali valori.

I valori di colore correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa ed esponenti non specificati. I componenti dei colori interi senza segno, se specificati, vengono mappati linearmente a valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 a 0,0 (intensità zero). Se specificato, i componenti di colore di interi con segno vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. Si noti che questo mapping non converte 0 esattamente in 0,0. I valori a virgola mobile vengono mappati direttamente.

Né i valori integer a virgola mobile né con segno vengono aggiornati all'intervallo \[ 0,1 prima \] dell'aggiornamento del colore corrente. Tuttavia, i componenti di colore vengono ancorati a questo intervallo prima che siano interpolati o scritti in un buffer di colori.

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

 

 





