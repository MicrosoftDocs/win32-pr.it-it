---
title: Classe ReplicationProvider1
description: Classe base per l'istanza del provider.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Classe ReplicationProvider1 Active Directory
- Classe ReplicationProvider1 Active Directory, descritta
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048270"
---
# <a name="replicationprovider1-class"></a>Classe ReplicationProvider1

Classe base per l'istanza del provider.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a>Members

La classe **ReplicationProvider1** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ReplicationProvider1** dispone di queste proprietà.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identificatore di classe utilizzato da WMI per determinare se caricare o meno un provider a prestazioni elevate nel processo client o nel processo WMI. Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe. Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI. WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.

Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**GUID** che rappresenta l'identificatore di classe (**CLSID**) dell'oggetto com del provider. Questo oggetto COM deve contenere un'implementazione dell'interfaccia [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Concorrenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identifica il computer in cui avviare il provider. Se il provider viene eseguito nel computer locale, è **null**.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, questa istanza è abilitata e può essere utilizzata per completare le richieste del client.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
</dt> </dl>

Contiene il modello di hosting del provider.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Riservato. Il valore predefinito è zero (0).

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Set di flag che forniscono informazioni sulla serializzazione. Il valore predefinito è zero (0).

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Tutte le inizializzazioni del provider devono essere serializzate.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Tutte le inizializzazioni del provider nello stesso spazio dei nomi devono essere serializzate.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


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

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**Windows Server 2003:** Questa proprietà è disabilitata.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nome provider.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider viene inizializzato per ogni impostazione locale quando un utente si connette allo stesso spazio dei nomi più di una volta utilizzando impostazioni locali diverse. Il valore predefinito è **false**.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider viene inizializzato una volta per ogni utente di NT LAN Manager (NTLM) che effettua richieste al provider. Se **false** (impostazione predefinita), il provider viene inizializzato una volta per tutti gli utenti.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Puro**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider accetta di preparare lo scaricamento chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in attesa quando WMI chiama il metodo **Release** della relativa interfaccia principale. I provider che devono rimanere client di WMI dopo che non funzionano come provider devono impostare **pure** su **false**. L'impostazione predefinita è **true**. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Descrittore di sicurezza (SD) nel linguaggio SDDL (Security Descriptor Definition Language) che determina il set di utenti che possono chiamare correttamente [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) per il provider disaccoppiato. Per ulteriori informazioni, vedere l'argomento [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nella sezione security del Windows SDK. Questo descrittore di sicurezza viene usato solo per i provider disaccoppiati e non influisce su altri provider. Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

WMI esegue controlli di accesso per i provider disaccoppiati che utilizzano le interfacce [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) . Se il descrittore di sicurezza è **null**, solo le applicazioni o i servizi eseguiti con gli account LocalSystem, NetworkService e LocalService possono eseguire un provider disaccoppiato.

La stringa seguente mostra un provider disaccoppiato che deve essere eseguito solo dagli amministratori predefiniti ". O:BAG: BAD: (A;; 0 X1;;; BA) "

Per ulteriori informazioni sull'impostazione della proprietà **securityDescriptor** , vedere [gestione della sicurezza WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

[Formato di data e ora](/windows/desktop/WmiSdk/date-and-time-format) che specifica per quanto tempo WMI consente al provider di rimanere inattivo prima che venga scaricato. In genere, i provider richiedono che WMI attenda non più di cinque minuti.

Per la versione corrente di WMI, il valore di questa proprietà viene ignorato. WMI Scarica il provider in base al valore di timeout in una classe interna nello \\ spazio dei nomi radice. È consigliabile che i provider impostino **UnloadTimeout**. Per ulteriori informazioni, vedere [scaricamento di un provider](/windows/desktop/WmiSdk/unloading-a-provider).

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Versione del provider. Le versioni supportate sono 1 e 2. La versione 2 rafforza i controlli di validità per tutte le registrazioni delle proprietà associate, in particolare la proprietà [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .

Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'istanza di questa classe rappresenta il provider WMI per Dominio di Active Directory Services. I valori predefiniti sono

-   Nome = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

