---
description: La \_ struttura dell'intestazione non elaborata WIA \_ definisce un'immagine nel formato dati non elaborati di un dispositivo e consente alle applicazioni di utilizzare il formato non elaborato nei trasferimenti WIA (Windows Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Struttura WIA_RAW_HEADER (Wiadef. h)
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
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307307"
---
# <a name="wia_raw_header-structure"></a>\_Struttura di intestazione non elaborata WIA \_

La struttura dell' **\_ \_ intestazione non elaborata WIA** definisce un'immagine nel formato dati non elaborati di un dispositivo e consente alle applicazioni di utilizzare il formato non elaborato nei trasferimenti WIA (Windows Image Acquisition).

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

Nome del formato. Deve essere il valore letterale ' WRAW ' (caratteri ASCII a byte singolo).

</dd> <dt>

**Versione**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versione del formato non elaborato. Usare sempre 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Byte totali validi nell'intestazione.

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

**Stampa**
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

Numero di byte in una riga di un'immagine non compressa. Utilizzare 0 quando i dati vengono compressi per segnalare che il numero di byte per riga è sconosciuto.

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

\_Tipo di dati IPA WIA \_ dell'immagine. Poiché \_ il formato dell'IPA WIA \_ è impostato su WiaImgFmt \_ RAW, si tratta di un elenco di valori consentiti da cui l'applicazione sceglie.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Numero di bit in un canale, fino a un massimo di 8.

</dd> <dt>

**Compressione**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Un valore di compressione del pacchetto WIA che \_ \_ specifica il tipo di compressione usato, se presente.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

\_ \_ Valore interp della fotometria IPA WIA che \_ specifica l'interpretazione fotometrica dell'immagine.

</dd> <dt>

**LineOrder**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore che rappresenta l'ordine di riga dell'immagine. Si tratta sempre dell' \_ ordine della riga WIA \_ \_ dall'alto \_ verso il \_ basso o \_ \_ \_ dal basso \_ verso l'alto nell'ordine della riga \_ .

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posizione dei dati dell'immagine non elaborata in byte, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui termina la tavolozza.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, dei dati dell'immagine non elaborata.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posizione della tavolozza in byte, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui terminano i dati. (Questo valore è 0, se non è presente alcuna tavolozza).

</dd> <dt>

**PaletteSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, della tabella della tavolozza. (Questo è 0, se non è presente alcuna tavolozza).

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché non si tratta di un formato di file, utilizzare una stringa vuota per \_ la \_ proprietà dell'estensione del file IPA WIA \_ .

La tavolozza e i dati possono essere in qualsiasi ordine.

**RawDataSize** non include l'intestazione o la tavolozza. Utilizzare questo campo per verificare che il trasferimento dell'immagine abbia avuto esito positivo.

**PaletteSize** è byte, non il numero di voci nella tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




