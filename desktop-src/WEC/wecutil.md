---
title: Wecutil.exe
description: Wecutil.exe è un'utilità raccolta eventi di Windows che consente a un amministratore di creare e gestire le sottoscrizioni agli eventi da origini eventi remote che supportano il protocollo di WS-Management.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353981"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe è un'utilità raccolta eventi di Windows che consente a un amministratore di creare e gestire le sottoscrizioni agli eventi da origini eventi remote che supportano il protocollo di WS-Management. I comandi, le opzioni e i valori di opzione non fanno distinzione tra maiuscole e minuscole per questa utilità.

Se viene visualizzato un messaggio che indica che il server RPC non è disponibile o che l'interfaccia è sconosciuta, quando si tenta di eseguire wecutil, è necessario avviare il servizio raccolta eventi Windows (wecsvc). Per avviare wecsvc, a un prompt dei comandi con privilegi elevati, digitare **net start wecsvc**.

## <a name="list-existing-subscriptions"></a>Elencare le sottoscrizioni esistenti

La sintassi seguente consente di elencare le sottoscrizioni di eventi remoti esistenti.

``` syntax
wecutil { es | enum-subscription }
```

Se si usa uno script per ottenere i nomi delle sottoscrizioni dall'output, sarà necessario ignorare i caratteri DBA UTF-8 nella prima riga dell'output. Nello script seguente viene illustrato un esempio di come è possibile ignorare i caratteri DBA.

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>Ottenere la configurazione della sottoscrizione

La sintassi seguente consente di visualizzare i dati di configurazione della sottoscrizione di eventi remoti.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Ottenere i parametri di configurazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**VALORE/f: ****
</dt> <dd>

Valore che specifica l'output dei dati di configurazione della sottoscrizione. Il valore può essere "XML" o "conciso" e il *valore* predefinito è "conciso". Se il *valore* è "XML", l'output viene stampato in formato "XML". Se il *valore* è "conciso", l'output viene stampato in coppie nome-valore.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valore***
</dt> <dd>

Valore che specifica se l'output è in formato Unicode. Il *valore* può essere "true" o "false". Se il *valore* è "true", l'output è in formato Unicode e se *value* è "false", l'output non è in formato Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Ottenere lo stato di runtime della sottoscrizione

La sintassi seguente consente di visualizzare lo stato di runtime della sottoscrizione.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Ottieni parametri di stato

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_origine evento**
</dt> <dd>

Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi. Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Impostare le informazioni di configurazione della sottoscrizione

La sintassi seguente viene utilizzata per impostare i dati di configurazione della sottoscrizione modificando i parametri di sottoscrizione dalla riga di comando o utilizzando un file di configurazione XML.

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>Commenti

Quando si specifica un nome utente o una password non corretta nel comando **wecutil SS** , non viene segnalato alcun errore fino a quando non si visualizza lo stato di runtime della sottoscrizione usando il comando **wecutil gr** .

## <a name="set-configuration-parameters"></a>Imposta parametri di configurazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *\_ file CONGIG***
</dt> <dd>

Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione. Il percorso può essere assoluto o relativo alla directory corrente. Questo parametro può essere utilizzato solo con i parametri facoltativi/CUS e/Cup e si escludono a vicenda con tutti gli altri parametri.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valore***
</dt> <dd>

Valore che determina se abilitare o disabilitare la sottoscrizione. Il valore può essere true o false. Il valore predefinito è true, che Abilita la sottoscrizione.

> [!Note]  
> Quando si disabilita una sottoscrizione avviata dall'agente di raccolta, l'origine evento diventa inattiva invece che disabilitata. In una sottoscrizione avviata dall'agente di raccolta è possibile disabilitare un'origine evento indipendente dalla sottoscrizione.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descrizione***
</dt> <dd>

Valore che specifica una descrizione per la sottoscrizione di eventi.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *data e \_ ora***
</dt> <dd>

Valore che specifica l'ora di scadenza della sottoscrizione. *Data di scadenza \_ TIME* è un valore specificato nel formato di data e ora standard XML o ISO8601: "aaaa-mm-ggThh: mm: SS \[ . sss \] \[ Z \] " dove "T" è il separatore dell'ora e "Z" indica l'ora UTC. Se, ad esempio, *data e \_ ora* è "2007-01-12T01:20:00", l'ora di scadenza della sottoscrizione è il 12 gennaio 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***
</dt> <dd>

Valore che specifica il tipo di eventi utilizzati dalla sottoscrizione. L'indirizzo del computer di origine evento insieme all'URI (Uniform Resource Identifier) identifica in modo univoco l'origine degli eventi. La stringa URI è utilizzata per tutti gli indirizzi di origine evento nella sottoscrizione.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modalità di configurazione***
</dt> <dd>

Valore che specifica la modalità di configurazione della sottoscrizione di eventi. *Configurazione \_ di La modalità* può essere una delle seguenti stringhe: "Normal", "Custom", "MinLatency" o "MinBandwidth". L'enumerazione della [**\_ modalità di \_ configurazione \_ della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) definisce le modalità di configurazione. È possibile specificare i parametri/DM,/DMI,/Hi e/DMLT solo se la modalità di configurazione è impostata su Custom.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *query***
</dt> <dd>

Valore che specifica la stringa di query per la sottoscrizione. Il formato di questa stringa può essere diverso per i diversi valori URI e si applica a tutte le origini eventi nella sottoscrizione.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *dialetto***
</dt> <dd>

Valore che specifica il dialetto utilizzato dalla stringa di query.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *Format***
</dt> <dd>

Valore che specifica il formato degli eventi restituiti. *Format* può essere "Events" o "informazioni sulla". Quando il valore è "informazioni sulla", gli eventi vengono restituiti con le stringhe localizzate, ad esempio le stringhe di descrizione evento, associate agli eventi. Il valore predefinito di *Format* è "informazioni sulla".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *impostazioni locali***
</dt> <dd>

Valore che specifica le impostazioni locali per il recapito delle stringhe localizzate nel formato di testo di cui è stato eseguito il rendering. Le *impostazioni locali* sono un identificatore di lingua/paese, ad esempio, "en-US". Questo parametro è valido solo quando il parametro/CF è impostato su "informazioni sulla".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *valore*\]**
</dt> <dd>

Valore che specifica gli eventi da recapitare per la sottoscrizione. Il *valore* può essere true o false. Quando *value* è true, tutti gli eventi esistenti vengono letti dalle origini eventi della sottoscrizione. Quando *value* è false, vengono recapitati solo gli eventi future (in arrivo). Il valore predefinito è true se/Ree viene specificato senza un valore e il valore predefinito è false se/Ree non è specificato.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *nomefile***
</dt> <dd>

Valore che specifica il registro eventi locale utilizzato per archiviare gli eventi ricevuti dalla sottoscrizione dell'evento.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *server di pubblicazione***
</dt> <dd>

Valore che specifica il nome dell'autore di eventi (provider). Deve essere un server di pubblicazione che possiede o importa il log specificato dal parametro/LF.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modalità***
</dt> <dd>

Valore che specifica la modalità di recapito della sottoscrizione. La *modalità* può essere push o pull. Questa opzione è valida solo se il parametro/cm è impostato su Custom.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *numero***
</dt> <dd>

Valore che specifica il numero massimo di elementi per il recapito in batch nella sottoscrizione dell'evento. Questa opzione è valida solo se il parametro/cm è impostato su Custom.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/DMLT: *MS***
</dt> <dd>

Valore che specifica la latenza massima consentita per la distribuzione di un batch di eventi. MS è il numero di millisecondi consentiti. Questo parametro è valido solo se il parametro/cm è impostato su Custom.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***
</dt> <dd>

Valore che specifica l'intervallo di heartbeat per la sottoscrizione. *MS* è il numero di millisecondi utilizzati nell'intervallo. Questo parametro è valido solo se il parametro/cm è impostato su Custom.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TRANSportaname***
</dt> <dd>

Valore che specifica il nome del trasporto utilizzato per la connessione al computer di origine dell'evento remoto.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *\_ origine evento***
</dt> <dd>

Valore che specifica l'indirizzo di un computer di origine evento. *Evento \_ SOURCE* è una stringa che identifica un computer di origine evento utilizzando il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP. Questo parametro può essere utilizzato con i parametri/ESE,/AES,/res o/un e/up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *valore***
</dt> <dd>

Valore che determina se abilitare o disabilitare un'origine evento. Il *valore* può essere true o false. Il valore predefinito è true, che Abilita l'origine evento. Questo parametro viene usato solo se viene usato il parametro/ESA.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Valore che aggiunge l'origine evento specificata dal parametro/ESA se l'origine evento non fa già parte della sottoscrizione di eventi. Se il computer specificato dal parametro/ESA fa già parte della sottoscrizione, viene visualizzato un errore. Questo parametro è consentito solo se viene usato il parametro/ESA.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Valore che rimuove l'origine evento specificata dal parametro/ESA se l'origine evento fa già parte della sottoscrizione di eventi. Se il computer specificato dal parametro/ESA non fa parte della sottoscrizione, viene visualizzato un errore. Questo parametro è consentito solo se viene usato il parametro/ESA.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nomeutente***
</dt> <dd>

Valore che specifica il nome utente utilizzato nelle credenziali per la connessione all'origine evento specificata nel parametro/ESA. Questo parametro è consentito solo se viene usato il parametro/ESA.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *password***
</dt> <dd>

Valore che specifica la password per il nome utente specificato nel parametro/un. Le credenziali relative al nome utente e alla password vengono usate per connettersi all'origine evento specificata nel parametro/ESA. Questo parametro è consentito solo se viene usato il parametro/un.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***
</dt> <dd>

Valore che specifica il numero di porta utilizzato dal trasporto quando ci si connette a un computer di origine evento remoto.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nome***
</dt> <dd>

Valore che specifica il nome DNS del computer locale. Questo nome viene utilizzato dalle origini eventi Remote per eseguire il push degli eventi e deve essere utilizzato solo per le sottoscrizioni push.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***
</dt> <dd>

Valore che specifica il tipo di credenziale utilizzato per l'accesso alle origini eventi remote. *Type* può essere "default", "Negotiate", "digest", "Basic" o "LocalMachine". Il valore predefinito è "default". Questi valori sono definiti nell'enumerazione [**del \_ \_ \_ tipo di credenziali della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nomeutente***
</dt> <dd>

Valore che imposta le credenziali utente condivise utilizzate per le origini eventi che non dispongono di credenziali utente personalizzate.

> [!Note]  
> Se questo parametro viene utilizzato con l'opzione/c, le impostazioni relative a nome utente e password per le singole origini eventi del file di configurazione verranno ignorate. Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri/un e/up per un'origine evento specifica nella riga di comando di un altro comando set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *password***
</dt> <dd>

Valore che imposta la password utente per le credenziali utente condivise. Quando la *password* è impostata su \* (asterisco), la password viene letta dalla console. Questa opzione è valida solo quando viene specificato il parametro/CUN.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *identificazione personale***
</dt> <dd>

Valore che imposta l'elenco di stampe Thumb del certificato dell'autorità emittente, in un elenco delimitato da virgole.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/As: *consentito***
</dt> <dd>

Valore che imposta un elenco delimitato da virgole di stringa che specifica i nomi DNS dei computer non di dominio a cui è consentito avviare le sottoscrizioni. I nomi possono essere specificati utilizzando caratteri jolly, ad esempio " \* . mydomain.com". Per impostazione predefinita, tale elenco è vuoto.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *negato***
</dt> <dd>

Valore che imposta un elenco delimitato da virgole di stringa che specifica i nomi DNS dei computer non di dominio che non sono autorizzati ad avviare le sottoscrizioni. I nomi possono essere specificati utilizzando caratteri jolly, ad esempio " \* . mydomain.com". Per impostazione predefinita, tale elenco è vuoto.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***
</dt> <dd>

Valore che imposta una stringa, in formato SDDL, che specifica quali computer del dominio sono consentiti o meno per avviare le sottoscrizioni. Il valore predefinito è consentire a tutti i computer del dominio di avviare le sottoscrizioni.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Creare una nuova sottoscrizione

La sintassi seguente consente di creare una sottoscrizione di eventi per gli eventi in un computer remoto.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Commenti

Quando si specifica un nome utente o una password non corretta nel comando **wecutil CS** , non viene segnalato alcun errore fino a quando non si visualizza lo stato di runtime della sottoscrizione usando il comando **wecutil gr** .

## <a name="creation-parameters"></a>Parametri di creazione

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**FILE di configurazione \_**
</dt> <dd>

Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione. Il percorso può essere assoluto o relativo alla directory corrente.

Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'agente di raccolta per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che consente di creare una sottoscrizione avviata dall'origine per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> Quando si crea una sottoscrizione avviata dall'origine, se **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** e **DeniedSubjectList** sono tutti vuoti, viene fornito un valore predefinito per **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ". Questa impostazione predefinita SDDL concede i membri del gruppo di dominio computer del dominio, nonché il gruppo di servizi di rete locale (per il server d'invio locale), la possibilità di generare eventi per questa sottoscrizione.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nomeutente***
</dt> <dd>

Valore che imposta le credenziali utente condivise utilizzate per le origini eventi che non dispongono di credenziali utente personalizzate. Questo valore si applica solo alle sottoscrizioni avviate dall'agente di raccolta.

> [!Note]  
> Se si specifica questo parametro, le impostazioni relative a nome utente e password per le singole origini eventi del file di configurazione verranno ignorate. Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri/un e/up per un'origine evento specifica nella riga di comando di un altro comando set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *password***
</dt> <dd>

Valore che imposta la password utente per le credenziali utente condivise. Quando la *password* è impostata su " \* " (asterisco), la password viene letta dalla console. Questa opzione è valida solo quando viene specificato il parametro/CUN.

</dd> </dl>

## <a name="delete-a-subscription"></a>Eliminare una sottoscrizione

La sintassi seguente consente di eliminare una sottoscrizione di eventi.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Parametri di eliminazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione. La sottoscrizione identificata in questo parametro verrà eliminata.

</dd> </dl>

## <a name="retry-a-subscription"></a>Ritentare una sottoscrizione

La sintassi seguente consente di ritentare una sottoscrizione inattiva tentando di riattivare tutte o origini eventi specificate stabilendo una connessione a ogni origine evento e inviando una richiesta di sottoscrizione remota all'origine evento. Le origini evento disabilitate non vengono ritentate.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Parametri di ripetizione dei tentativi

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione. Verrà eseguito un nuovo tentativo di sottoscrizione identificata in questo parametro.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_origine evento**
</dt> <dd>

Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi. Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configurare il servizio raccolta eventi di Windows

La sintassi seguente viene utilizzata per configurare il servizio raccolta eventi di Windows per garantire che le sottoscrizioni di eventi possano essere create e sostenute attraverso il riavvio del computer. Sono incluse le procedure seguenti:

**Per configurare il servizio raccolta eventi di Windows**

1.  Attivare il canale ForwardedEvents se è disabilitato.
2.  Ritardare l'avvio del servizio raccolta eventi di Windows.
3.  Se non è in esecuzione, avviare il servizio Raccolta eventi Windows.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configurare i parametri dell'agente di raccolta eventi

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valore***
</dt> <dd>

Valore che determina se il comando di configurazione rapida richiederà una conferma. Il valore può essere true o false. Se il valore è true, il comando richiederà una conferma. Il valore predefinito è false.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

 





