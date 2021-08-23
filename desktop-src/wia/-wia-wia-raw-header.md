---
description: La struttura WIA RAW HEADER definisce un'immagine nel formato dati RAW di un dispositivo e consente alle applicazioni di usare il formato RAW nei trasferimenti \_ \_ WIA (Windows Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER struttura (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 2b4e89f47737788fa9ebf238f06f6420eafbc31d7b27ab7933372d0716fb6588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812951"
---
# <a name="wia_raw_header-structure"></a>Struttura WIA \_ RAW \_ HEADER

La **struttura WIA \_ RAW \_ HEADER** definisce un'immagine nel formato dati RAW di un dispositivo e consente alle applicazioni di usare il formato RAW nei trasferimenti WIA (Windows Image Acquisition).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Tag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nome del formato. Deve essere il valore letterale "WRAW" (quattro caratteri ASCII a byte singolo).

</dd> <dt>

**Version**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versione del formato RAW. Usare sempre 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Totale dei byte validi nell'intestazione.

</dd> <dt>

**XRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Risoluzione orizzontale espressa in punti per pollice.

</dd> <dt>

**YRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Risoluzione verticale espressa in punti per pollice.

</dd> <dt>

**XExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Larghezza dell'immagine in pixel.

</dd> <dt>

**YExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Altezza dell'immagine in pixel.

</dd> <dt>

**BytesPerLine**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di byte in una riga di un'immagine non compressa. Usare 0 quando i dati vengono compressi per segnalare che il numero di byte per riga è sconosciuto.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero totale di bit per pixel per tutti i canali del pixel.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di canali di colore in un pixel.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

DATATYPE IPA WIA \_ \_ dell'immagine. Poiché WIA IPA FORMAT è impostato su \_ WiaImgFmt RAW, si tratta di un elenco di valori consentiti da cui \_ \_ l'applicazione sceglie.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Numero di bit in un canale, fino a un massimo di 8.

</dd> <dt>

**Compressione**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore WIA IPA COMPRESSION che specifica il tipo di compressione \_ \_ usato, se presente.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore WIA \_ IPA \_ PHOTOMETRIC \_ INTERP che specifica l'interpretazione fotometrica dell'immagine.

</dd> <dt>

**LineOrder**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore che rappresenta l'ordine delle righe dell'immagine. Si tratta sempre di WIA \_ LINE ORDER TOP TO BOTTOM o \_ \_ \_ \_ WIA LINE ORDER BOTTOM \_ TO \_ \_ \_ \_ TOP.

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posizione in byte dei dati di immagine non elaborati, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui termina il riquadro.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, dei dati dell'immagine non elaborati.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posizione del riquadro in byte, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui terminano i dati. Questo valore è 0, se non è presente alcun riquadro.

</dd> <dt>

**PaletteSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni, in byte, della tabella del riquadro. È 0, se non è presente alcun riquadro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché non si tratta di un formato di file, usare una stringa vuota per la proprietà \_ WIA IPA \_ FILE \_ EXTENSION.

La tavolozza e i dati possono essere in entrambi gli ordini.

**RawDataSize** non include l'intestazione o il riquadro. Usare questo campo per verificare che il trasferimento dell'immagine abbia avuto esito positivo.

**PaletteSize** è byte, non il numero di voci nel riquadro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




