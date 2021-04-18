---
description: Per la registrazione di un consumer di eventi permanenti è necessaria un'istanza della \_ \_ classe di sistema eventfilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314607"
---
# <a name="__eventfilter-class"></a>\_\_Classe EventFilter

Per la registrazione di un consumer di eventi permanenti è necessaria un'istanza della classe di sistema **\_ \_ EventFilter** .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventFilter** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventFilter** dispone di queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea il filtro. In Strumentazione gestione Windows (WMI) viene archiviato il SID dell'utente che crea un'istanza di **\_ \_ EventFilter** o il SID Administrator, a seconda del sistema operativo. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Descrittore di sicurezza (SD) in Security Descriptor Definition Language (SDDL) che controlla l'accesso agli eventi recapitati al filtro. Usare questa proprietà per specificare che solo gli eventi nel contesto di sicurezza di account specifici possono essere recapitati a questo filtro. Un consumer di eventi permanenti può ad esempio cancellare i registri di sicurezza solo quando un determinato evento viene generato da un utente specifico. Per specificare gli utenti che possono pubblicare eventi in questo filtro, usare la maschera di **\_ \_ pubblicazione a destra WBEM** nella voce di controllo di accesso (ACE) per la proprietà del [**\_ descrittore di sicurezza**](--event.md) . Per ulteriori informazioni, vedere [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md). Per ulteriori informazioni ed esempi, vedere Replace:[ricezione di eventi](receiving-events-securely.md)in modo sicuro.

È possibile configurare un descrittore di sicurezza per l'accesso agli eventi per consentire il recapito di un evento solo quando l'account di sistema locale genera l'evento. Per ulteriori informazioni sulla creazione di un descrittore di sicurezza e l'autorizzazione dell'accesso, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Esempio: la stringa SDDL seguente consente solo agli amministratori di fornire eventi al filtro. Il diritto necessario per fornire gli eventi è **WBEM \_ right \_ Publish** (X80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Spazio dei nomi dell'istanza di evento utilizzata per le sottoscrizioni tra gli spazi dei nomi.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Identificatore univoco di un filtro evento. Poiché un filtro eventi viene utilizzato solo internamente da WMI, è consigliabile impostare questa proprietà su un identificatore univoco globale (**GUID**) convertito in una stringa. Tuttavia, i consumer possono utilizzare qualsiasi schema privato per un nome di filtro, purché non esista un conflitto con altri filtri.

</dd> <dt>

**Query**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Query di evento WQL (Strumentazione gestione Windows Query Language) che specifica il set di eventi per la notifica del consumer e le condizioni specifiche per la notifica.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Lingua utilizzata per la query. Poiché WMI supporta attualmente solo WMI Query Language (WQL) come linguaggio di query, questa proprietà deve essere impostata su "WQL".

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ EventFilter** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md).

## <a name="examples"></a>Esempio

Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ EventFilter** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Creazione di un filtro eventi](creating-an-event-filter.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 

