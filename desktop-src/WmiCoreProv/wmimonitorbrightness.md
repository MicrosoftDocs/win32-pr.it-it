---
description: Rappresenta i parametri di luminosità di un monitor del computer.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Classe WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317606"
---
# <a name="wmimonitorbrightness-class"></a>Classe WmiMonitorBrightness

La classe WMI **WmiMonitorBrightness** rappresenta i parametri di luminosità di un monitor del computer.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Members

La classe **WmiMonitorBrightness** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorBrightness** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il monitoraggio di destinazione è attivo.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Luminosità corrente. Questo valore deve essere un valore tratto dai *livelli*.

Esempio: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: chiave
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente i livelli di luminosità possibili.

Esempio: \[ 0, 1, 2,..., 100 \] .

</dd> <dt>

**Livelli**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero totale di livelli di luminosità supportati dal monitoraggio, come descritto in *Level*.

Esempio: 101

</dd> </dl>

## <a name="examples"></a>Esempio

Per altre informazioni ed esempi di codice sull'uso di questa classe in PowerShell, vedere [usare PowerShell per segnalare e impostare la luminosità del monitoraggio](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).

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

 

 




