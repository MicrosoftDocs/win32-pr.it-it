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
ms.openlocfilehash: 10343b33e5bc1881440af9d13029913d470880289e71b4c7a33fb4748e56ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821522"
---
# <a name="wmimonitorbrightness-class"></a>Classe WmiMonitorBrightness

La **classe WMI WmiMonitorBrightness** rappresenta i parametri di luminosità di un monitor del computer.

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

La **classe WmiMonitorBrightness** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorBrightness** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il monitoraggio di destinazione è attivo.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Luminosità corrente. Questo valore deve essere un valore derivato da *Levels.*

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

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente i livelli di luminosità possibili.

Esempio: \[ 0, 1, 2, ..., 100 \] .

</dd> <dt>

**Livelli**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di livelli di luminosità supportati dal monitor, come descritto in *Livello*.

Esempio: 101

</dd> </dl>

## <a name="examples"></a>Esempio

Per altre informazioni ed esempi di codice sull'uso di questa classe in PowerShell, vedere Usare PowerShell per creare [report e impostare la luminosità del monitoraggio.](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)

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

 

 




