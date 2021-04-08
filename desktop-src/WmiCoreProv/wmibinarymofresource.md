---
description: Il provider di classi WDM definisce la classe WMIBinaryMofResource nello \\ \\ spazio dei nomi WMI radice per supportare l'attività di tenere traccia dello stato dei dati nel repository WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Classe WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879974"
---
# <a name="wmibinarymofresource-class"></a>Classe WMIBinaryMofResource

Il provider di classi WDM definisce la classe **WMIBinaryMofResource** nello \\ \\ spazio dei nomi WMI radice per supportare l'attività di tenere traccia dello stato dei dati nel repository WMI.

## <a name="syntax"></a>Sintassi

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Members

La classe **WMIBinaryMofResource** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WMIBinaryMofResource** dispone di queste proprietà.

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Metà alta dell'indicatore di data e ora.

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Metà inferiore dell'indicatore di data e ora.

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Flag che indica se il file con estensione MOF è stato elaborato completamente.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nome del driver WDM abilitato con un file MOF binario compilato correttamente nel repository WMI.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider di classi WDM crea un'istanza di **WMIBinaryMofResource** per ogni driver WDM che fornisce un file MOF binario.

Ogni volta che WMI inizializza il provider, il provider confronta il timestamp con il timestamp del file di immagine del driver. Se i timestamp sono diversi, WMI ricompila nuovamente il file MOF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                     |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider WDM](wdm-provider.md)
</dt> </dl>

 

