---
description: Rappresenta la gestione del controllo del computer (CMC) corretta da passare dal driver di interrupt al polling. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
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
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343446"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>\_Classe MSMCAEvent SwitchToCMCPolling

La classe **MSMCAEvent \_ SwitchToCMCPolling** rappresenta la gestione del controllo del computer (CMC) corretta da passare dal driver di interrupt al polling. In alcuni casi, il kernel esegue il polling di System Abstraction Layer (SAL) per qualsiasi CMC o errore di piattaforma (CPE) corretto che si è verificato nell'intervallo di polling precedente. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **classe \_ SwitchToCMCPolling di MSMCAEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SwitchToCMCPolling di MSMCAEvent** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza della classe è attiva; in caso contrario, **false**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificatore univoco di questa istanza della classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MSMCAEvent \_ SwitchToCMCPolling** è derivata da [**WmiEvent**](wmievent.md).

System Abstraction Layer (SAL) è il codice bruciato su ROM che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma. È simile al BIOS su una piattaforma x86. Nei casi in cui la piattaforma non supporta gli interrupt per il polling CMC o CPE, il sistema operativo esegue il polling ogni minuto, controllando se si è verificato un errore in precedenza. Se la piattaforma supporta le interruzioni e il sistema operativo riceve una quantità definita dall'utente di sondaggi CMC o CPE entro un minuto, Disabilita l'interrupt e il polling. Se l'utente non definisce il numero di polling entro un minuto, il sistema imposta un valore predefinito di 10 poll al minuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

