---
description: Rappresenta la gestione del controllo del computer corretta da passare dal driver di interrupt al polling. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640941"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>Classe MSMCAEvent \_ SwitchToCMCPolling

La **classe MSMCAEvent \_ SwitchToCMCPolling** rappresenta la gestione corretta del controllo del computer (CMC) da passare dal driver di interrupt al polling. In alcuni casi, il kernel esegue il polling del livello di astrazione del sistema (SAL) per qualsiasi CMC o errore di piattaforma (CPE) corretto che si è verificato nell'intervallo di polling precedente. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **classe MSMCAEvent \_ SwitchToCMCPolling** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ SwitchToCMCPolling** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**TRUE** se questa istanza della classe è attiva; in caso contrario, **FALSE.**

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificatore univoco di questa istanza della classe .

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ SwitchToCMCPolling** è derivata da [**WMIEvent.**](wmievent.md)

Il livello di astrazione del sistema (SAL, System Abstraction Layer) è un frammento di codice che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma. È simile al BIOS in una piattaforma x86. Nei casi in cui la piattaforma non supporta interrupt per il polling CMC o CPE, il sistema operativo esegue il polling ogni minuto, verificando se si è verificato un errore in precedenza. Se la piattaforma supporta interrupt e il sistema operativo riceve una quantità definita dall'utente di polling CMC o CPE entro un minuto, l'interrupt e il polling vengono disabilitati. Se l'utente non definisce il numero di sondaggi entro un minuto, il sistema imposta un valore predefinito su 10 sondaggi al minuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

