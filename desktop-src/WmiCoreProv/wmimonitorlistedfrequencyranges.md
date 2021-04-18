---
description: Elenca gli intervalli di frequenza supportati dal monitoraggio.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Classe WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314100"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>Classe WmiMonitorListedFrequencyRanges

La classe WMI **WmiMonitorListedFrequencyRanges** elenca gli intervalli di frequenza supportati dal monitoraggio. Questi intervalli si trovano nella definizione del video di input del blocco EDID (video Electronics Standard Association) Enhanced Extended Display Identification Data (E-) o nel file INF di Windows che contiene i dati del driver di dispositivo.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Members

La classe **WmiMonitorListedFrequencyRanges** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorListedFrequencyRanges** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **FrequencyRangeDescriptor**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di intervalli di frequenza di monitoraggio rappresentati da istanze della classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di intervalli di frequenza di monitoraggio supportati elencati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




