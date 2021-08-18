---
description: 'Image_V1_Load classe: questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load classe
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
ms.openlocfilehash: 35144317b67a8d24ec07d72633897366e83628d6cc66d9c4661980fc44c373b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070161"
---
# <a name="image_v1_load-class"></a>Classe Load \_ dell'immagine V1 \_

Questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini.

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

La **classe Image \_ V1 \_ Load** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Image \_ V1 \_ Load** ha queste proprietà.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Indirizzo di base dell'applicazione in cui viene caricata l'immagine.

</dd> <dt>

Imagesize
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Puntatore
</dt> </dl>

Dimensioni dell'immagine caricata.

Quando si utilizza questa proprietà, il tipo di dati per questa proprietà è effettivamente size \_ t. Il qualificatore Pointer viene usato per determinare se la dimensione \_ t è di 4 byte o 8 byte.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Identifica il processo in cui viene caricata l'immagine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 




