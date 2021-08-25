---
description: Registra informazioni sull'implementazione fisica di un provider in WMI. I provider che non impostano la proprietà HostingModel vengono caricati, per impostazione predefinita, per l'esecuzione in un processo Wmiprvse.exe come NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dd7c848e9c792bcff3c0af58143d404bda744a982daeedbff01895242407a7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857691"
---
# <a name="__win32provider-class"></a>\_\_Classe Win32Provider

La **\_ \_ classe di sistema Win32Provider** registra informazioni sull'implementazione fisica di un provider in WMI. I provider che non impostano la proprietà **HostingModel** vengono caricati, per impostazione predefinita, per l'esecuzione in un processo Wmiprvse.exe **come NetworkServiceHostOrSelfHost**.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe Win32Provider** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe Win32Provider** ha queste proprietà.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Identificatore di classe utilizzato da WMI per determinare se caricare o meno un provider a prestazioni elevate nel processo client o nel processo WMI. Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe. Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI. WMI usa anche **ClientLoadableCLSID per** supportare le operazioni di aggiornamento.

Per altre informazioni, vedere [Registrazione di un provider High-Performance distribuzione.](registering-a-high-performance-provider.md)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

**GUID** che rappresenta l'identificatore di classe (**CLSID**) dell'oggetto COM del provider. Questo oggetto COM deve contenere un'implementazione [**dell'interfaccia IWbemProviderInit.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)

</dd> <dt>

**Concorrenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Identifica il computer in cui avviare il provider. Se il provider viene eseguito nel computer locale, è **NULL.**

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** questa istanza è abilitata e può essere usata per completare le richieste client.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Questa proprietà è costituita dai valori delle proprietà **HostingGroup e** **HostingSpecification** dei provider [**MSFT. \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) Il valore di questa proprietà specifica il modo in cui WMI carica il provider e l'account di sicurezza con cui viene eseguito. Per altre informazioni sull'impostazione della **proprietà HostingModel,** vedere [Hosting e sicurezza del provider](provider-hosting-and-security.md) e Registrazione di un [provider.](registering-a-provider.md)

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Riservato. Il valore predefinito è zero (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Set di flag che forniscono informazioni sulla serializzazione. Il valore predefinito è zero (0).

<dt>

0
</dt> <dd>

Tutte le inizializzazioni di questo provider devono essere serializzate.

</dd> <dt>

1
</dt> <dd>

Tutte le inizializzazioni di questo provider nello stesso spazio dei nomi devono essere serializzate.

</dd> <dt>

2
</dt> <dd>

Non è necessaria alcuna serializzazione di inizializzazione.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

DA DEFINIRE

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **Chiave**](standard-qualifiers.md)
</dt> </dl>

Nome provider.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** il provider viene inizializzato per ogni impostazione locale quando un utente si connette più volte allo stesso spazio dei nomi usando impostazioni locali diverse. Il valore predefinito è **FALSE.**

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** il provider viene inizializzato una volta per ogni utente NT LAN Manager (NTLM) che effettua richieste al provider. Se **FALSE** (impostazione predefinita), il provider viene inizializzato una sola volta per tutti gli utenti.

</dd> <dt>

**Puro**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** il provider accetta di prepararsi per lo scaricamento chiamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in sospeso quando WMI chiama il metodo **Release** della relativa interfaccia primaria. I provider che devono rimanere client di WMI dopo che non funzionano come provider devono **impostare Pure** su **FALSE.** L'impostazione predefinita è **TRUE.** Per altre informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Descrittore di sicurezza (SD) nel linguaggio SDDL (Security Descriptor Definition Language) che determina il set di utenti che possono chiamare correttamente [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) per il provider disaccoccodato. Per altre informazioni, vedere [l'argomento Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nella sezione Security di Windows SDK. Questo descrittore di sicurezza viene utilizzato solo per i provider disaccoccodati e non influisce su altri provider. Per altre informazioni, vedere [Incorporamento di un provider in un'applicazione.](incorporating-a-provider-in-an-application.md)

WMI esegue controlli di accesso per i provider disaccoccodati che usano le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink.**](iwbemobjectsink.md) Se il descrittore di sicurezza è **NULL,** solo le applicazioni o i servizi eseguiti con gli account LocalSystem, NetworkService e LocalService possono eseguire un provider disaccoccodato.

La stringa seguente mostra un provider disaccoccodato che deve essere eseguito solo dagli amministratori predefiniti." O:BAG:BAD:(A;;0 x1;;; BA)"

Per altre informazioni sull'impostazione **della proprietà SecurityDescriptor,** vedere [Gestione della sicurezza WMI.](maintaining-wmi-security.md)

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

[Formato di data e ora](date-and-time-format.md) che specifica per quanto tempo WMI consente al provider di rimanere inattivo prima di essere scaricato. In genere, i provider richiedono che WMI attenda non più di cinque minuti.

Per la versione corrente di WMI, il valore di questa proprietà viene ignorato. WMI scarica il provider in base al valore di timeout in una classe interna nello spazio \\ dei nomi radice. È consigliabile che i provider **impostano UnloadTimeout**. Per altre informazioni, vedere [Scaricamento di un provider.](unloading-a-provider.md)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Versione del provider. Le versioni supportate sono 1 e 2. La versione 2 potenzia i controlli di validità per tutte le registrazioni di proprietà associate, in particolare la [**proprietà ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe Win32Provider** è derivata dal [**\_ \_ provider**](--provider.md).

La maggior parte dei provider può accettare i valori predefiniti **per la proprietà InitializationReentrancy.** Tuttavia, se un provider può supportare l'inizializzazione simultanea per utenti separati, questa proprietà può essere impostata su 1 (uno). Se è necessaria l'inizializzazione serializzata, **InitializationReentrancy** rimane 0 (zero). In entrambi i **casi, PerUserInitialization** è impostato su **TRUE.**

Un provider puro o un provider che imposta la **proprietà Pure** su **TRUE** esiste solo per le richieste di servizio provenienti da applicazioni e WMI. La maggior parte dei provider sono provider puri. Un provider non di servizio è l'eccezione. I provider non di utilizzo passano al ruolo del client dopo aver completato le richieste di manutenzione.

Un esempio di provider non di utilizzo è un provider push che inizia a inviare query e invia richieste di WMI dopo il completamento dell'inizializzazione. Un provider di push non ha responsabilità se non aggiornare il repository CIM con i dati in fase di inizializzazione. Dopo l'aggiornamento del repository, un provider di push può attendere lo scaricarsi o passare al ruolo del client. Il provider di push in attesa di essere scaricato è un provider puro. Il provider di push che partecipa alle attività client non è di servizio.

WMI deve essere in grado di distinguere i provider puri dai provider non puri in modo che possa determinare quando è sicuro arrestare. WMI deve attendere il completamento di tutte le operazioni che coinvolgono provider non puri prima di poter essere arrestato in modo sicuro.

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

 

