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
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106499"
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

Quando si utilizza questa proprietà, il tipo di dati per questa proprietà è effettivamente size \_ t. Il qualificatore puntatore viene usato per determinare se la dimensione \_ t è di 4 o 8 byte.

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
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 




