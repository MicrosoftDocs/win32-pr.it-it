---
description: La struttura DIBDATA contiene informazioni su una bitmap indipendente dal dispositivo (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Struttura DIBDATA (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330659"
---
# <a name="dibdata-structure"></a>Struttura DIBDATA

La `DIBDATA` struttura contiene informazioni su una bitmap indipendente dal dispositivo (DIB) GDI.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**PaletteVersion**
</dt> <dd>

Questo membro deve essere incrementato ogni volta che la tavolozza viene modificata.

</dd> <dt>

**DibSection**
</dt> <dd>

Struttura **DIBSection** che contiene informazioni sulla DIB. Per informazioni dettagliate, vedere la documentazione di GDI.

</dd> <dt>

**hBitmap**
</dt> <dd>

Handle per la bitmap.

</dd> <dt>

**hMapping**
</dt> <dd>

Handle per un oggetto mapping di file utilizzato per condividere la memoria tra GDI e un oggetto [**CImageSample**](cimagesample.md) .

</dd> <dt>

**pBase**
</dt> <dd>

Indirizzo della bitmap.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl> |



 

 




