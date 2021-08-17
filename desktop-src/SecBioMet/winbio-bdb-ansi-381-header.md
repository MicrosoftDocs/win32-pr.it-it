---
title: WINBIO_BDB_ANSI_381_HEADER struttura (Winbio \_ types.h)
description: Specifica informazioni su una serie di campioni di impronta digitale o palmo.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc9eee5d3ca99799c76b849e7b990eee2b94c61309c4d729f736ad33a00eecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911279"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>Struttura WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER

La **struttura WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER** specifica informazioni su una serie di campioni di impronta digitale o palmo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Recordlength**
</dt> <dd>

Dimensioni, in byte, di questa struttura più le dimensioni di tutte le strutture [**WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD**](winbio-bdb-ansi-381-record.md) per i campioni di impronta digitale o palmo acquisiti da un utente finale. Sono validi solo i sei byte bassi.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Specifica il formato. Attualmente, questa operazione deve essere 0x46495200.

</dd> <dt>

**Versionnumber**
</dt> <dd>

Specifica il numero di versione. Attualmente deve essere 0x30313000 che corrisponde internamente a 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Struttura [**WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) che contiene il formato dei dati registrati come coppia proprietario/tipo.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Contiene l'ID unità del dispositivo usato per acquisire l'esempio.

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

Specifica il livello di risoluzione in corrispondenza del quale viene acquisito l'esempio.

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

Specifica la risoluzione orizzontale dell'analisi.

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

Specifica la risoluzione verticale dell'analisi.

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

Specifica la risoluzione orizzontale dell'impronta digitale acquisita o dell'immagine del palmo.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Specifica la risoluzione verticale dell'impronta digitale acquisita o dell'immagine del palmo.

</dd> <dt>

**ElementCount**
</dt> <dd>

Numero di record di dito o palmo in questa struttura .

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Contiene l'unità di misura, 1 per pollici e 2 per centimetri.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Specifica il numero di bit in un pixel. Può essere da 1 a 16 bit per pixel per il colore.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Specifica l'algoritmo utilizzato per comprimere l'immagine del dito o del palmo.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





