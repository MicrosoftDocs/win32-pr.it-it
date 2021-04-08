---
description: Registra le informazioni sull'implementazione fisica di un provider in WMI. I provider che non impostano la proprietà HostingModel vengono caricati per impostazione predefinita per l'esecuzione in un processo di Wmiprvse.exe come NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968374"
---
# <a name="__win32provider-class"></a>\_\_Classe Win32Provider

La classe di sistema **\_ \_ Win32Provider** registra informazioni sull'implementazione fisica di un provider in WMI. I provider che non impostano la proprietà **HostingModel** vengono caricati per impostazione predefinita per l'esecuzione in un processo di Wmiprvse.exe come **NetworkServiceHostOrSelfHost**.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a>Members

La classe **\_ \_ Win32Provider** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ Win32Provider** dispone di queste proprietà.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identificatore di classe utilizzato da WMI per determinare se caricare o meno un provider a prestazioni elevate nel processo client o nel processo WMI. Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe. Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI. WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.

Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance.](registering-a-high-performance-provider.md)

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**GUID** che rappresenta l'identificatore di classe (**CLSID**) dell'oggetto com del provider. Questo oggetto COM deve contenere un'implementazione dell'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .

</dd> <dt>

**Concorrenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identifica il computer in cui avviare il provider. Se il provider viene eseguito nel computer locale, è **null**.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, questa istanza è abilitata e può essere utilizzata per completare le richieste del client.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Questa proprietà è costituita dai valori delle proprietà **HostingGroup** e **HostingSpecification** dei [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) . Il valore di questa proprietà specifica il modo in cui WMI carica il provider e l'account di sicurezza in cui viene eseguito. Per ulteriori informazioni sull'impostazione della proprietà **HostingModel** , vedere [hosting e sicurezza del provider](provider-hosting-and-security.md) e [registrazione di un provider](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Riservato. Il valore predefinito è zero (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Set di flag che forniscono informazioni sulla serializzazione. Il valore predefinito è zero (0).

<dt>

0
</dt> <dd>

Tutte le inizializzazioni del provider devono essere serializzate.

</dd> <dt>

1
</dt> <dd>

Tutte le inizializzazioni del provider nello stesso spazio dei nomi devono essere serializzate.

</dd> <dt>

2
</dt> <dd>

Non è necessaria alcuna serializzazione dell'inizializzazione.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

TBD

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Nome provider.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider viene inizializzato per ogni impostazione locale quando un utente si connette allo stesso spazio dei nomi più di una volta utilizzando impostazioni locali diverse. Il valore predefinito è **false**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider viene inizializzato una volta per ogni utente di NT LAN Manager (NTLM) che effettua richieste al provider. Se **false** (impostazione predefinita), il provider viene inizializzato una volta per tutti gli utenti.

</dd> <dt>

**Puro**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider accetta di preparare lo scaricamento chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in attesa quando WMI chiama il metodo **Release** della relativa interfaccia principale. I provider che devono rimanere client di WMI dopo che non funzionano come provider devono impostare **pure** su **false**. L'impostazione predefinita è **true**. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Descrittore di sicurezza (SD) nel linguaggio SDDL (Security Descriptor Definition Language) che determina il set di utenti che possono chiamare correttamente [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) per il provider disaccoppiato. Per ulteriori informazioni, vedere l'argomento [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nella sezione security del Windows SDK. Questo descrittore di sicurezza viene usato solo per i provider disaccoppiati e non influisce su altri provider. Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).

WMI esegue controlli di accesso per i provider disaccoppiati che utilizzano le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](iwbemobjectsink.md) . Se il descrittore di sicurezza è **null**, solo le applicazioni o i servizi eseguiti con gli account LocalSystem, NetworkService e LocalService possono eseguire un provider disaccoppiato.

La stringa seguente mostra un provider disaccoppiato che deve essere eseguito solo dagli amministratori predefiniti ". O:BAG: BAD: (A;; 0 X1;;; BA) "

Per ulteriori informazioni sull'impostazione della proprietà **securityDescriptor** , vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

[Formato di data e ora](date-and-time-format.md) che specifica per quanto tempo WMI consente al provider di rimanere inattivo prima che venga scaricato. In genere, i provider richiedono che WMI attenda non più di cinque minuti.

Per la versione corrente di WMI, il valore di questa proprietà viene ignorato. WMI Scarica il provider in base al valore di timeout in una classe interna nello \\ spazio dei nomi radice. È consigliabile che i provider impostino **UnloadTimeout**. Per ulteriori informazioni, vedere [scaricamento di un provider](unloading-a-provider.md).

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Versione del provider. Le versioni supportate sono 1 e 2. La versione 2 rafforza i controlli di validità per tutte le registrazioni delle proprietà associate, in particolare la proprietà [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ Win32Provider** è derivata dal [**\_ \_ provider**](--provider.md).

La maggior parte dei provider può accettare i valori predefiniti per la proprietà **InitializationReentrancy** . Tuttavia, se un provider è in grado di supportare l'inizializzazione simultanea per utenti distinti, questa proprietà può essere impostata su 1 (uno). Se è necessaria l'inizializzazione serializzata, **InitializationReentrancy** rimane 0 (zero). In entrambe le istanze, **PerUserInitialization** è impostato su **true**.

Un provider pure o un provider che imposta la proprietà **pure** su **true** esiste solo per le richieste di servizio da applicazioni e WMI. La maggior parte dei provider sono provider puri. Un provider non pure è l'eccezione. I provider non puri passano al ruolo di client dopo aver completato le richieste di manutenzione.

Un esempio di provider non pure è un provider di push che inizia a eseguire query ed effettua richieste di WMI dopo aver completato l'inizializzazione. Un provider di push non ha responsabilità ad eccezione dell'aggiornamento del repository CIM con i dati in fase di inizializzazione. Dopo l'aggiornamento del repository, un provider di push può rimanere in attesa di essere scaricato o passare al ruolo del client. Il provider di push che attende di essere scaricato è un provider puro. Il provider di push che partecipa alle attività del client non è puro.

WMI deve essere in grado di distinguere i provider puri da provider non puri, in modo che sia possibile determinare quando è sicuro arrestarsi. WMI deve attendere il completamento di tutte le operazioni che coinvolgono provider non puri prima che sia possibile arrestarlo in modo sicuro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Provider**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> </dl>

 

