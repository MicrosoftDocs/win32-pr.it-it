---
title: Wecutil.exe
description: Wecutil.exe è un'Windows agente di raccolta eventi che consente a un amministratore di creare e gestire sottoscrizioni a eventi inoltrati da origini eventi remote che supportano il protocollo WS-Management.
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
ms.openlocfilehash: 6e93e09bc4eed51448b686f0d18f00ecacaacd31d063c4905757d0185128ee64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750971"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe è un'Windows agente di raccolta eventi che consente a un amministratore di creare e gestire sottoscrizioni a eventi inoltrati da origini eventi remote che supportano il protocollo WS-Management. Per questa utilità, per i comandi, le opzioni e i valori delle opzioni non viene fatto distinzione tra maiuscole e minuscole.

Se viene visualizzato il messaggio "Il server RPC non è disponibile" o "L'interfaccia è sconosciuta" quando si tenta di eseguire wecutil, è necessario avviare il servizio agente di raccolta eventi di Windows (wecsvc). Per avviare wecsvc, al prompt dei comandi con privilegi elevati digitare **net start wecsvc**.

## <a name="list-existing-subscriptions"></a>Elencare le sottoscrizioni esistenti

La sintassi seguente viene usata per elencare le sottoscrizioni di eventi remoti esistenti.

``` syntax
wecutil { es | enum-subscription }
```

Se si usa uno script per ottenere i nomi delle sottoscrizioni dall'output, sarà necessario ignorare i caratteri UTF-8 BOM nella prima riga dell'output. Lo script seguente mostra un esempio di come ignorare i caratteri BOM.

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

La sintassi seguente viene usata per visualizzare i dati di configurazione della sottoscrizione di eventi remoti.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Ottenere i parametri di configurazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID SOTTOSCRIZIONE**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato **nell'elemento SubscriptionId** del file di configurazione XML usato per creare la sottoscrizione.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:*VALUE***
</dt> <dd>

Valore che specifica l'output dei dati di configurazione della sottoscrizione. *VALUE* può essere "XML" o "Terse" e il valore predefinito è "Terse". Se *VALUE* è "XML", l'output viene stampato in formato "XML". Se *VALUE* è "Terse", l'output viene stampato in coppie nome-valore.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***
</dt> <dd>

Valore che specifica se l'output è in formato Unicode. *VALUE* può essere "true" o "false". Se *VALUE* è "true", l'output è in formato Unicode e se *VALUE* è "false", l'output non è in formato Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Ottenere lo stato di runtime della sottoscrizione

La sintassi seguente viene usata per visualizzare lo stato di runtime della sottoscrizione.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Ottenere i parametri di stato

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID SOTTOSCRIZIONE**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato **nell'elemento SubscriptionId** del file di configurazione XML usato per creare la sottoscrizione.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**ORIGINE \_ EVENTO**
</dt> <dd>

Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi. Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Impostare le informazioni di configurazione della sottoscrizione

La sintassi seguente viene utilizzata per impostare i dati di configurazione della sottoscrizione modificando i parametri della sottoscrizione dalla riga di comando o usando un file di configurazione XML.

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

Quando si specifica un nome utente o una password non corretta nel comando **wecutil ss,** non viene segnalato alcun errore finché non si visualizza lo stato di runtime della sottoscrizione usando il **comando wecutil gr.**

## <a name="set-configuration-parameters"></a>Impostare i parametri di configurazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID SOTTOSCRIZIONE**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato **nell'elemento SubscriptionId** del file di configurazione XML usato per creare la sottoscrizione.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *FILE \_ CONGIG***
</dt> <dd>

Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione. Il percorso può essere assoluto o relativo alla directory corrente. Questo parametro può essere usato solo con i parametri facoltativi /cus e /cup e si escludono a vicenda con tutti gli altri parametri.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***
</dt> <dd>

Valore che determina se abilitare o disabilitare la sottoscrizione. VALUE può essere true o false. Il valore predefinito è true, che abilita la sottoscrizione.

> [!Note]  
> Quando si disabilita una sottoscrizione avviata dall'agente di raccolta, l'origine evento diventa inattiva anziché disabilitata. In una sottoscrizione avviata dall'agente di raccolta è possibile disabilitare un'origine evento indipendentemente dalla sottoscrizione.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***
</dt> <dd>

Valore che specifica una descrizione per la sottoscrizione di eventi.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE \_ TIME***
</dt> <dd>

Valore che specifica l'ora di scadenza della sottoscrizione. *DATE \_ TIME* è un valore specificato nel formato di data/ora XML standard o ISO8601: "aaaa-MM-ggThh:mm:ss \[ .sss Z", dove "T" è il separatore dell'ora e \] \[ \] "Z" indica l'ora UTC. Ad esempio, se *DATE \_ TIME* è "2007-01-12T01:20:00", l'ora di scadenza della sottoscrizione è il 12 gennaio 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***
</dt> <dd>

Valore che specifica il tipo di eventi utilizzati dalla sottoscrizione. L'indirizzo del computer di origine eventi insieme all'URI (Uniform Resource Identifier) identifica in modo univoco l'origine degli eventi. La stringa URI è utilizzata per tutti gli indirizzi di origine evento nella sottoscrizione.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *MODALITÀ DI \_ CONFIGURAZIONE***
</dt> <dd>

Valore che specifica la modalità di configurazione della sottoscrizione di eventi. *CONFIGURAZIONE \_ MODE* può essere una delle stringhe seguenti: "Normal", "Custom", "MinLatency" o "MinBandwidth". [**L'enumerazione EC SUBSCRIPTION CONFIGURATION \_ \_ \_ MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) definisce le modalità di configurazione. I parametri /dm, /dmi, /hi e /dmlt possono essere specificati solo se la modalità di configurazione è impostata su Personalizzata.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***
</dt> <dd>

Valore che specifica la stringa di query per la sottoscrizione. Il formato di questa stringa può essere diverso per valori URI diversi e si applica a tutte le origini evento nella sottoscrizione.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***
</dt> <dd>

Valore che specifica il dialetto utilizzato dalla stringa di query.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***
</dt> <dd>

Valore che specifica il formato degli eventi restituiti. *FORMAT* può essere "Events" o "RenderedText". Quando il valore è "RenderedText", gli eventi vengono restituiti con le stringhe localizzate ,ad esempio le stringhe di descrizione degli eventi, associate agli eventi. Il valore predefinito di *FORMAT* è "RenderedText".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***
</dt> <dd>

Valore che specifica le impostazioni locali per il recapito delle stringhe localizzate in formato testo sottoposto a rendering. *LOCALE* è un identificatore di impostazioni cultura di lingua/paese, ad esempio "EN-us". Questo parametro è valido solo quando il /cf parametro è impostato su "RenderedText".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree: \[ *VALUE*\]**
</dt> <dd>

Valore che specifica quali eventi devono essere recapitati per la sottoscrizione. *VALUE* può essere true o false. Quando *VALUE* è true, tutti gli eventi esistenti vengono letti dalle origini eventi della sottoscrizione. Quando *VALUE* è false, vengono recapitati solo gli eventi futuri (in arrivo). Il valore predefinito è true quando /ree viene specificato senza un valore e il valore predefinito è false se /ree non è specificato.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***
</dt> <dd>

Valore che specifica il registro eventi locale utilizzato per archiviare gli eventi ricevuti dalla sottoscrizione di eventi.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***
</dt> <dd>

Valore che specifica il nome dell'autore (provider) dell'evento. Deve essere un server di pubblicazione proprietario o importato del log specificato dal parametro /lf.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***
</dt> <dd>

Valore che specifica la modalità di recapito della sottoscrizione. *MODE* può essere push o pull. Questa opzione è valida solo se il /cm parametro è impostato su Personalizzato.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***
</dt> <dd>

Valore che specifica il numero massimo di elementi per il recapito in batch nella sottoscrizione di eventi. Questa opzione è valida solo se il /cm parametro è impostato su Personalizzato.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Valore che specifica la latenza massima consentita per il recapito di un batch di eventi. MS è il numero di millisecondi consentiti. Questo parametro è valido solo se il /cm parametro è impostato su Personalizzato.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***
</dt> <dd>

Valore che specifica l'intervallo di heartbeat per la sottoscrizione. *MS* è il numero di millisecondi utilizzati nell'intervallo. Questo parametro è valido solo se il /cm parametro è impostato su Personalizzato.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***
</dt> <dd>

Valore che specifica il nome del trasporto utilizzato per connettersi al computer di origine eventi remoto.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *ORIGINE \_ EVENTO***
</dt> <dd>

Valore che specifica l'indirizzo di un computer di origine eventi. *EVENTO \_ SOURCE* è una stringa che identifica un computer di origine eventi utilizzando il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP. Questo parametro può essere usato con i parametri /ese, /aes, /res o /un e /up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***
</dt> <dd>

Valore che determina se abilitare o disabilitare un'origine evento. *VALUE* può essere true o false. Il valore predefinito è true, che abilita l'origine evento. Questo parametro viene usato solo se si usa il parametro /esa.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Valore che aggiunge l'origine evento specificata dal parametro /esa se l'origine evento non fa già parte della sottoscrizione di eventi. Se il computer specificato dal /esa parametro fa già parte della sottoscrizione, viene visualizzato un errore. Questo parametro è consentito solo se viene usato il parametro /esa.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Valore che rimuove l'origine evento specificata dal parametro /esa se l'origine evento fa già parte della sottoscrizione di eventi. Se il computer specificato dal /esa parametro non fa parte della sottoscrizione, viene visualizzato un errore. Questo parametro è consentito solo se viene usato il parametro /esa.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *NOME UTENTE***
</dt> <dd>

Valore che specifica il nome utente utilizzato nelle credenziali per connettersi all'origine evento specificata nel parametro /esa. Questo parametro è consentito solo se viene usato il parametro /esa.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***
</dt> <dd>

Valore che specifica la password per il nome utente specificato nel parametro /un. Le credenziali del nome utente e della password vengono usate per connettersi all'origine evento specificata nel parametro /esa. Questo parametro è consentito solo se viene usato il parametro /un.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***
</dt> <dd>

Valore che specifica il numero di porta utilizzato dal trasporto per la connessione a un computer di origine eventi remoto.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***
</dt> <dd>

Valore che specifica il nome DNS del computer locale. Questo nome viene usato dalle origini eventi remote per eseguire il push degli eventi e deve essere usato solo per le sottoscrizioni push.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***
</dt> <dd>

Valore che specifica il tipo di credenziale utilizzato per accedere alle origini eventi remote. *TYPE* può essere "default", "negotiate", "digest", "basic" o "localmachine". Il valore predefinito è "default". Questi valori sono definiti [**nell'enumerazione EC SUBSCRIPTION \_ \_ CREDENTIALS \_ TYPE.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Valore che imposta le credenziali utente condivise utilizzate per le origini evento che non dispongono delle proprie credenziali utente.

> [!Note]  
> Se questo parametro viene usato con l'opzione /c , le impostazioni relative a nome utente e password per le singole origini evento del file di configurazione vengono ignorate. Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri /un e /up per un'origine evento specifica nella riga di comando di un altro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Valore che imposta la password utente per le credenziali utente condivise. Quando *l'opzione PASSWORD* è \* impostata su (asterisco), la password viene letta dalla console. Questa opzione è valida solo quando viene specificato il parametro /cun.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *IDENTIFICAZIONI PERSONALE***
</dt> <dd>

Valore che imposta l'elenco di stampe del certificato dell'autorità di certificazione, in un elenco delimitato da virgole.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***
</dt> <dd>

Valore che imposta un elenco delimitato da virgole di stringhe che specificano i nomi DNS dei computer non di dominio a cui è consentito avviare sottoscrizioni. I nomi possono essere specificati usando caratteri jolly, ad esempio \* ".mydomain.com". Per impostazione predefinita, tale elenco è vuoto.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***
</dt> <dd>

Valore che imposta un elenco delimitato da virgole di stringhe che specificano i nomi DNS dei computer non di dominio a cui non è consentito avviare sottoscrizioni. I nomi possono essere specificati usando caratteri jolly, ad esempio \* ".mydomain.com". Per impostazione predefinita, tale elenco è vuoto.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***
</dt> <dd>

Valore che imposta una stringa, in formato SDDL, che specifica quali computer di dominio sono autorizzati o meno ad avviare sottoscrizioni. L'impostazione predefinita consente a tutti i computer di dominio di avviare le sottoscrizioni.

> [!Note]  
> Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Creare una nuova sottoscrizione

La sintassi seguente viene usata per creare una sottoscrizione di eventi per gli eventi in un computer remoto.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Commenti

Quando viene specificato un nome utente o una password non corretta nel comando **wecutil cs,** non viene segnalato alcun errore fino a quando non si visualizza lo stato di runtime della sottoscrizione usando il **comando wecutil gr.**

## <a name="creation-parameters"></a>Parametri di creazione

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**FILE DI \_ CONFIGURAZIONE**
</dt> <dd>

Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione. Il percorso può essere assoluto o relativo alla directory corrente.

Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'agente di raccolta per inoltrare gli eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.


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



Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'origine per inoltrare gli eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.


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
> Quando si crea una sottoscrizione avviata dall'origine, se **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** IssuerCAList, AllowedSubjectList e DeniedSubjectList sono tutti vuoti, verrà fornito un valore predefinito per /  **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;  GA; ; ;D C)(A;; GA;;; NS)". Questo SDDL concede ai membri del gruppo di dominio Domain Computers, nonché al gruppo di servizi di rete locale (per il server d'inoltro locale), la possibilità di generare eventi per questa sottoscrizione.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Valore che imposta le credenziali utente condivise utilizzate per le origini evento che non dispongono delle proprie credenziali utente. Questo valore si applica solo alle sottoscrizioni avviate dall'agente di raccolta.

> [!Note]  
> Se questo parametro viene specificato, le impostazioni relative a nome utente e password per le singole origini evento del file di configurazione vengono ignorate. Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri /un e /up per un'origine evento specifica nella riga di comando di un altro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Valore che imposta la password utente per le credenziali utente condivise. Quando *PASSWORD* è impostato su " \* " (asterisco), la password viene letta dalla console. Questa opzione è valida solo quando viene specificato il parametro /cun.

</dd> </dl>

## <a name="delete-a-subscription"></a>Eliminare una sottoscrizione

La sintassi seguente viene usata per eliminare una sottoscrizione di eventi.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Parametri di eliminazione

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID SOTTOSCRIZIONE**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato **nell'elemento SubscriptionId** del file di configurazione XML usato per creare la sottoscrizione. La sottoscrizione identificata in questo parametro verrà eliminata.

</dd> </dl>

## <a name="retry-a-subscription"></a>Ritentare una sottoscrizione

La sintassi seguente viene usata per ritentare una sottoscrizione inattiva provando a riattivare tutte le origini eventi o specificate stabilendo una connessione a ogni origine evento e inviando una richiesta di sottoscrizione remota all'origine evento. Le origini evento disabilitate non vengono ritentate.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Parametri di ripetizione dei tentativi

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID SOTTOSCRIZIONE**
</dt> <dd>

Stringa che identifica in modo univoco una sottoscrizione. Questo identificatore viene specificato **nell'elemento SubscriptionId** del file di configurazione XML usato per creare la sottoscrizione. La sottoscrizione identificata in questo parametro verrà ritentata.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**ORIGINE \_ EVENTO**
</dt> <dd>

Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi. Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configurare il servizio Windows agente di raccolta eventi

La sintassi seguente viene usata per configurare il Windows agente di raccolta eventi per garantire che le sottoscrizioni di eventi possano essere create e sostenute tramite riavvii del computer. È inclusa la procedura seguente:

**Per configurare il Windows agente di raccolta eventi**

1.  Attivare il canale ForwardedEvents se è disabilitato.
2.  Ritardare l'avvio del Windows agente di raccolta eventi.
3.  Se non è in esecuzione, avviare il servizio Raccolta eventi Windows.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configurare i parametri dell'agente di raccolta eventi

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***
</dt> <dd>

Valore che determina se il comando quick-config richiederà la conferma. VALUE può essere true o false. Se VALUE è true, il comando richiederà la conferma. Il valore predefinito è false.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

 





