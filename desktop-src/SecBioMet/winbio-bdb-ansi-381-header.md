---
title: Struttura WINBIO_BDB_ANSI_381_HEADER ( \_ tipi WINBIO. h)
description: Specifica le informazioni su una serie di campioni di impronte digitali o di Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- Struttura di WINBIO_BDB_ANSI_381_HEADER Windows Biometric Framework API
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
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301636"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>\_Struttura dell'intestazione WINBIO BDB \_ ANSI \_ 381 \_

La struttura di **\_ intestazione WINBIO BDB \_ ANSI \_ 381 \_** specifica informazioni su una serie di campioni di impronte digitali o di Palm.

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

**RecordLength**
</dt> <dd>

Dimensione, in byte, della struttura più le dimensioni di tutte le strutture [**di \_ record WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) per gli esempi di impronte digitali o di Palma acquisiti da un utente finale. Solo i sei byte bassi sono validi.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Specifica il formato. Attualmente, deve essere 0x46495200.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Specifica il numero di versione. Attualmente deve essere 0x30313000 che corrisponde internamente a 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che contiene il formato dati registrato come coppia proprietario/tipo.

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

Specifica la risoluzione orizzontale dell'impronta digitale acquisita o dell'immagine Palm.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Specifica la risoluzione verticale dell'impronta digitale acquisita o dell'immagine Palm.

</dd> <dt>

**Valore elementCount**
</dt> <dd>

Numero di record del dito o della palma nella struttura.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Contiene l'unità di misura, 1 per i pollici e 2 per centimetri.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Specifica il numero di bit in un pixel. Questo può essere da 1 a 16 bit per pixel per il colore.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Specifica l'algoritmo usato per comprimere il dito o l'immagine Palm.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





