---
description: Questa classe è la classe del tipo di evento per il caricamento di immagini negli eventi di file di paging. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980087"
---
# <a name="pagefault_imageloadbacked-class"></a>\_Classe pagefault ImageLoadBacked

Questa classe è la classe del tipo di evento per il caricamento di immagini negli eventi di file di paging.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Members

La **classe \_ ImageLoadBacked di pagefault** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ImageLoadBacked di pagefault** dispone di queste proprietà.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Riservato.

</dd> <dt>

**Filechar**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Format ("x")
</dt> </dl>

Riservato.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento del [**\_ nome**](fileio-name.md) di FileIO per determinare il nome del file.

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), Format ("x")
</dt> </dl>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento viene registrato durante la creazione di una sezione di immagine, ad esempio il caricamento di una DLL, quando il gestore della memoria determina che l'immagine deve essere copiata ed eseguita dal file di paging. Le immagini vengono in genere eseguite dal file di origine, ma il file di paging può verificarsi quando il gestore della memoria determina che il file di origine può essere modificato in modo asincrono da Writer esistenti o quando il file di origine si trova in un supporto rimovibile o in un dispositivo remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




