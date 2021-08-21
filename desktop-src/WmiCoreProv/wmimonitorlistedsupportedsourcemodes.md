---
description: Elenca le modalità di origine supportate per un monitor video nel relativo descrittore di monitoraggio, se presenti.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Classe WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ca942fce42388eaeb2eb90b7b7ecd992dd6df39bca554bb63bbc55fb6bbb867a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821466"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>Classe WmiMonitorListedSupportedSourceModes

**WmiMonitorListedSupportedSourceModes** elenca le modalità di origine supportate per un monitor video nel relativo descrittore di monitoraggio, se presenti. Per i monitoraggi senza descrizione, questo elenco di modalità viene generato in base al tipo di monitoraggio, come specificato dal driver del bus di monitoraggio.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>Members

La **classe WmiMonitorListedSupportedSourceModes** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorListedSupportedSourceModes** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**MonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice VideoModeDescriptor**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenca le modalità di origine del monitoraggio rappresentate da istanze [**della classe VideoModeDescriptor.**](videomodedescriptor.md)

</dd> <dt>

**NumOfMonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di modalità di origine del monitoraggio supportate elencate.

</dd> <dt>

**PreferredMonitorSourceModeIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indice preferito della modalità di origine del monitoraggio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




