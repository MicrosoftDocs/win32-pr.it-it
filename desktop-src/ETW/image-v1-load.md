---
description: Questa classe è la classe del tipo di evento per gli eventi di caricamento di immagini. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Classe Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977119"
---
# <a name="image_v1_load-class"></a>\_Classe di \_ caricamento image V1

Questa classe è la classe del tipo di evento per gli eventi di caricamento di immagini.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Members

La classe di **\_ \_ caricamento image V1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Questa proprietà è **configurata nella classe di \_ \_ caricamento image V1** .

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.

</dd> <dt>

ImageBase sul
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo di base dell'applicazione in cui viene caricata l'immagine.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Dimensione dell'immagine da caricare.

Quando si utilizza questa proprietà, il tipo di dati per questa proprietà è effettivamente size \_ t. Il qualificatore del puntatore viene utilizzato per determinare se la dimensione \_ t è di 4 byte o 8 byte.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Identifica il processo in cui viene caricata l'immagine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 




