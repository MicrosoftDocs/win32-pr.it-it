---
title: Classe SystemRestoreConfig
description: Fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata in ogni unità.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Ripristino del sistema della classe SystemRestoreConfig
- Ripristino del sistema della classe SystemRestoreConfig, descritto
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400717"
---
# <a name="systemrestoreconfig-class"></a>Classe SystemRestoreConfig

Fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata in ogni unità.

## <a name="syntax"></a>Sintassi

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Members

La classe **SystemRestoreConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SystemRestoreConfig** dispone di queste proprietà.

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità massima di spazio su disco in ogni unità che può essere utilizzata da ripristino configurazione di sistema. Questo valore viene specificato come percentuale dello spazio totale dell'unità. Il valore predefinito è 12%.

**Windows Vista:** Riceve un valore dal Servizio Copia Shadow del volume (VSS). Questa è la quantità massima di spazio su disco in ogni unità che può essere usata da ripristino configurazione di sistema. Il valore predefinito è pari al 15% dello spazio totale dell'unità o al 30% dello spazio libero disponibile, a seconda del valore minore.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo assoluto in cui vengono creati i checkpoint di sistema pianificati, in secondi. Il valore predefinito è 86.400 (24 ore).

**Windows Vista:** Riceve un valore dall'utilità di pianificazione per ripristino configurazione di sistema. Zero se l'attività è disabilitata.

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo per il quale i punti di ripristino vengono conservati, in secondi. Quando un punto di ripristino diventa precedente a questo intervallo specificato, viene eliminato. Il limite di validità predefinito è 90 giorni.

**Windows Vista:** Riceve il valore **UINTMAX**.

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo in secondi durante il quale i checkpoint di sistema pianificati vengono creati durante la sessione. Il valore predefinito è zero, che indica che la funzionalità è disattivata.

**Windows Vista:** Riceve zero se ripristino configurazione di sistema è disabilitato.

</dd> </dl>

## <a name="examples"></a>Esempio

Il codice di esempio seguente non è supportato. Utilizzare lo strumento da riga di comando Vssadmin.exe per modificare la dimensione dello spazio riservato sull'unità.

**Windows XP:** Questo esempio è supportato.


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | \\Impostazioni predefinite radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Punti di ripristino](restore-points.md)
</dt> <dt>

[Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

