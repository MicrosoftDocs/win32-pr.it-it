---
description: 'Image_V0_Load: questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106515"
---
# <a name="image_v0_load-class"></a>Classe Image \_ V0 \_ Load

Questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Members

La **classe Image \_ V0 \_ Load** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Image \_ V0 \_ Load** ha queste proprietà.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Indirizzo di base dell'applicazione in cui viene caricata l'immagine.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.

</dd> <dt>

ModuleSize
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Dimensioni dell'immagine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine \_ V0**](image-v0.md)
</dt> </dl>

 

 




