---
description: Include opzioni che possono essere impostate o recuperate per la sessione corrente di Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Enumerazione WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051879"
---
# <a name="winhttprequestoption-enumeration"></a>Enumerazione WinHttpRequestOption

**L'enumerazione WinHttpRequestOption** include opzioni che possono essere impostate o recuperate per la sessione microsoft Windows servizi HTTP (WinHTTP) corrente.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**
</dt> <dd>

Imposta o recupera un elemento **VARIANT contenente** la stringa [*dell'agente*](glossary.md) utente.

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption \_ URL**
</dt> <dd>

Recupera un elemento **VARIANT** che contiene l'URL della risorsa. Questo valore è di sola lettura. Non è possibile impostare l'URL usando questa proprietà. L'URL non può essere letto fino a quando [**non viene chiamato**](iwinhttprequest-open.md) il metodo Open. Questa opzione è utile per controllare l'URL al termine [**del metodo Send**](iwinhttprequest-send.md) per verificare che si sia verificato un reindirizzamento.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

Imposta o recupera un elemento **VARIANT che** identifica la tabella [*codici per*](glossary.md) la stringa dell'URL. Il valore predefinito è la tabella codici UTF-8. La tabella codici viene usata per convertire la stringa URL Unicode, passata nel [**metodo Open,**](iwinhttprequest-open.md) in una rappresentazione di stringa a byte singolo.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Imposta o recupera un elemento **VARIANT che** indica se la percentuale di caratteri nella stringa URL viene convertita in una sequenza di escape. Il valore predefinito di questa opzione è **VARIANT \_ TRUE,** che specifica che tutti i caratteri ANSI (unsafe American National Standards Institute), ad eccezione del simbolo di percentuale, vengono convertiti in una sequenza di escape.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Imposta o recupera un elemento **VARIANT che** indica quali errori del certificato del server devono essere ignorati. Può trattarsi di una combinazione di uno o più dei flag seguenti.



| Errore                                                  | Valore  |
|--------------------------------------------------------|--------|
| Autorità di certificazione (CA) sconosciuta o radice non attendibile | 0x0100 |
| Utilizzo errato                                            | 0x0200 |
| Nome comune non valido                               | 0x1000 |
| Data o certificato scaduto non valido                    | 0x2000 |



 

Il valore predefinito di questa opzione nella versione 5.1 di WinHTTP è zero e non viene quindi ignorato alcun errore. Nelle versioni precedenti di WinHTTP, l'impostazione predefinita era 0x3300, il che ha comportato che tutti gli errori del certificato del server vengano ignorati per impostazione predefinita.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Imposta un **variant** che specifica il certificato client inviato a un server per l'autenticazione. Questa opzione indica il percorso, [*l'archivio*](glossary.md)certificati e il soggetto di un certificato client delimitato da barre rovesciate. Per altre informazioni sulla selezione di un certificato client, vedere [SSL in WinHTTP.](ssl-in-winhttp.md)

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Imposta o recupera un elemento **VARIANT** che indica se le richieste vengono reindirizzate automaticamente quando il server specifica un nuovo percorso per la risorsa. Il valore predefinito di questa opzione è **VARIANT \_ TRUE** per indicare che le richieste vengono reindirizzate automaticamente.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**UrlEscapeDisable di WinHttpRequestOption \_**
</dt> <dd>

Imposta o recupera un elemento **VARIANT che** indica se i caratteri non sicuri nei componenti di percorso e query di un URL vengono convertiti in sequenze di escape. Il valore predefinito di questa opzione è **VARIANT \_ TRUE,** che specifica che i caratteri nel percorso e nella query vengono convertiti.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Imposta o recupera un elemento **VARIANT che** indica se i caratteri non sicuri nel componente di query dell'URL vengono convertiti in sequenze di escape. Il valore predefinito di questa opzione è **VARIANT \_ TRUE,** che specifica che i caratteri nella query vengono convertiti.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Imposta o recupera un elemento **VARIANT** che indica quali protocolli sicuri possono essere utilizzati. Questa opzione consente di selezionare i protocolli accettabili per il client. Il protocollo viene negoziato durante l'handshake Secure Sockets Layer (SSL). Può trattarsi di una combinazione di uno o più dei flag seguenti.



| Protocollo                           | Valore  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Transport Layer Security (TLS) 1.0 | 0x0080 |



 

Il valore predefinito di questa opzione è 0x0028, che indica che è possibile usare SSL 2.0 o SSL 3.0. Se questa opzione è impostata su zero, il client e il [](iwinhttprequest-send.md) server non sono in grado di determinare un protocollo di sicurezza accettabile e il successivo invio restituisce un errore.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**
</dt> <dd>

Imposta o recupera un elemento **VARIANT** che indica se la traccia è attualmente abilitata. Per altre informazioni sulla funzionalità di traccia in Microsoft Windows HTTP Services (WinHTTP), vedere [Funzionalità di traccia WinHTTP.](winhttptracecfg-exe--a-trace-configuration-tool.md)

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Controlla se [**l'oggetto WinHttpRequest**](winhttprequest.md) ripristina temporaneamente la rappresentazione client per la durata delle operazioni di autenticazione del certificato SSL. L'impostazione predefinita per **l'oggetto WinHttpRequest** è **TRUE.** Impostare questa opzione su **FALSE per mantenere** la rappresentazione durante l'esecuzione di operazioni di autenticazione del certificato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Controlla se WinHTTP consente i reindirizzamenti. Per impostazione predefinita, tutti i reindirizzamenti vengono seguiti automaticamente, ad eccezione di quelli che vengono trasferiti da un URL sicuro (https) a un URL non sicuro (http). Impostare questa opzione su **TRUE per** abilitare i reindirizzamenti da HTTPS a HTTP.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Abilita o disabilita il supporto per l'autenticazione Passport. Per impostazione predefinita, il supporto automatico per l'autenticazione Passport è disabilitato. Impostare questa opzione su **TRUE per abilitare** il supporto dell'autenticazione Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Imposta o recupera il numero massimo di reindirizzamenti che WinHTTP segue; il valore predefinito è 10. Questo limite impedisce ai siti non autorizzati di bloccare il client WinHTTP dopo un numero elevato di reindirizzamenti.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Imposta o recupera un set associato sulla dimensione massima della parte di intestazione della risposta del server. Questo limite protegge il client da un server dannoso che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione. Il valore predefinito è 64 KB.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Imposta o recupera un limite sulla quantità di dati che verranno svuotati dalle risposte per riutilizzare una connessione. Il valore predefinito è 1 MB.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Imposta o recupera un valore booleano che indica se è necessario usare HTTP/1.1 o HTTP/1.0. Il valore predefinito **è TRUE,** pertanto per impostazione predefinita viene usato HTTP/1.1.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Abilita il controllo delle revoche di certificati del server durante la negoziazione SSL. Quando il server presenta un certificato, viene eseguito un controllo per determinare se il certificato è stato revocato dall'autorità emittente. Se il certificato viene effettivamente revocato o il controllo delle revoche non riesce perché non è possibile scaricare l'elenco di revoche di certificati (CRL), la richiesta ha esito negativo. Tali errori di revoca non possono essere eliminati.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Impostare un'opzione specificando una delle costanti precedenti come parametro della [**proprietà Option.**](iwinhttprequest-option.md)

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHttp.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




