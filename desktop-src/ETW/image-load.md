---
description: Questa classe è la classe del tipo di evento per gli eventi di immagine. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528651"
---
# <a name="image_load-class"></a>\_Classe di caricamento immagini

Questa classe è la classe del tipo di evento per gli eventi di immagine.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>Members

La classe di **\_ caricamento dell'immagine** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Questa proprietà è **configurata nella classe \_ Load** .

<dl> <dt>

DefaultBase
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), puntatore
</dt> </dl>

Indirizzo di base predefinito.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (12), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome file ed estensione della DLL o dell'immagine eseguibile.

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

ImageCheckSum
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Somma controllo immagine.

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

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6)
</dt> </dl>

Riservato.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (8)
</dt> </dl>

Riservato.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (9)
</dt> </dl>

Riservato.

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (10)
</dt> </dl>

Riservato.

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (11)
</dt> </dl>

Riservato.

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Data e ora in cui l'immagine è stata caricata o scaricata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli eventi DCStart e DCEnd enumerano tutte le immagini caricate rispettivamente all'inizio e alla fine della traccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine**](image.md)
</dt> <dt>

[**Immagine \_ V0**](image-v0.md)
</dt> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 




