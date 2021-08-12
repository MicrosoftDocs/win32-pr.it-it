---
description: La struttura DIBDATA contiene informazioni su una bitmap GDI indipendente dal dispositivo (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Struttura DIBDATA (Winutil.h)
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
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653819"
---
# <a name="dibdata-structure"></a>Struttura DIBDATA

La `DIBDATA` struttura contiene informazioni su una bitmap GDI indipendente dal dispositivo (DIB).

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

Questo membro deve essere incrementato ogni volta che il riquadro cambia.

</dd> <dt>

**DibSection**
</dt> <dd>

**Struttura DIBSECTION** che contiene informazioni sulla dib. Per informazioni dettagliate, vedere la documentazione di GDI.

</dd> <dt>

**Hbitmap**
</dt> <dd>

Handle per la bitmap.

</dd> <dt>

**hMapping**
</dt> <dd>

Handle a un oggetto di mapping di file usato per condividere la memoria tra GDI e un [**oggetto CImageSample.**](cimagesample.md)

</dd> <dt>

**Pbase**
</dt> <dd>

Indirizzo della bitmap.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl> |



 

 




