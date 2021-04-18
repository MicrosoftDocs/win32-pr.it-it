---
title: funzione glColor4ubv (GL. h)
description: Imposta il colore corrente da una matrice di valori di colore già esistente. | funzione glColor4ubv (GL. h)
ms.assetid: 6456e4c6-3d86-4555-863f-22e41a0d0018
keywords:
- funzione glColor4ubv OpenGL
topic_type:
- apiref
api_name:
- glColor4ubv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8612246a936b7d9e67c73d515f8856600805d24a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321384"
---
# <a name="glcolor4ubv-function"></a>glColor4ubv (funzione)

Imposta il colore corrente da una matrice di valori di colore già esistente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColor4ubv(
   const GLubyte *v
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

GL archivia sia un indice dei colori a valore singolo corrente sia un colore corrente RGBA a quattro valori. **glcolor** imposta un nuovo colore RGBA a quattro valori. **glcolor** presenta due varianti principali: **glcolor3** e **glcolor4**. le varianti **glcolor3** specificano i nuovi valori rosso, verde e blu in modo esplicito e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa). le varianti **glcolor4** specificano tutti e quattro i componenti colore in modo esplicito.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** accettano gli Integer a tre o quattro byte con segno, short o long come argomenti. Quando v viene aggiunto al nome, i comandi color possono assumere un puntatore a una matrice di tali valori.

I valori dei colori correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate. I componenti dei colori integer senza segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 sia mappato a 0,0 (intensità zero). I componenti di colore integer con segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a-1,0. Si noti che questo mapping non converte 0 esattamente in 0,0. Ai valori a virgola mobile viene eseguito il mapping diretto.

Nessun valore a virgola mobile né Signed Integer viene fissato all'intervallo \[ 0, 1 \] prima che venga aggiornato il colore corrente. Tuttavia, i componenti dei colori vengono fissati a questo intervallo prima che vengano interpolati o scritti in un buffer dei colori.

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





