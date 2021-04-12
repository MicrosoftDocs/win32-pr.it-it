---
description: Include le opzioni che è possibile impostare o recuperare per la sessione corrente dei servizi HTTP di Microsoft Windows (WinHTTP).
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
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526238"
---
# <a name="winhttprequestoption-enumeration"></a>Enumerazione WinHttpRequestOption

L'enumerazione **WinHttpRequestOption** include opzioni che è possibile impostare o recuperare per la sessione corrente dei servizi HTTP di Microsoft Windows (WinHTTP).

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

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**\_UserAgentString WinHttpRequestOption**
</dt> <dd>

Imposta o Recupera una **variante** che contiene la stringa dell' [*agente utente*](glossary.md) .

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL WinHttpRequestOption**
</dt> <dd>

Recupera una **variante** che contiene l'URL della risorsa. Questo valore è di sola lettura. non è possibile impostare l'URL utilizzando questa proprietà. L'URL non può essere letto finché non viene chiamato il metodo [**Open**](iwinhttprequest-open.md) . Questa opzione è utile per controllare l'URL dopo il completamento del metodo [**Send**](iwinhttprequest-send.md) per verificare che sia stato eseguito il reindirizzamento.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**\_URLCodePage WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un **Variant** che identifica la [*tabella codici*](glossary.md) per la stringa dell'URL. Il valore predefinito è la tabella codici UTF-8. La tabella codici viene utilizzata per convertire la stringa dell'URL Unicode, passata nel metodo [**Open**](iwinhttprequest-open.md) , a una rappresentazione di stringa a byte singolo.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**\_EscapePercentInURL WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica se la percentuale di caratteri nella stringa dell'URL viene convertita in una sequenza di escape. Il valore predefinito di questa opzione è **Variant \_ true** che specifica tutti i caratteri unsafe American National Standards Institute (ANSI) ad eccezione del fatto che il simbolo di percentuale viene convertito in una sequenza di escape.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**\_SslErrorIgnoreFlags WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica quali errori del certificato del server devono essere ignorati. Può trattarsi di una combinazione di uno o più dei flag seguenti.



| Errore                                                  | Valore  |
|--------------------------------------------------------|--------|
| Autorità di certificazione (CA) o radice non attendibile sconosciuta | 0x0100 |
| Utilizzo errato                                            | 0x0200 |
| Nome comune non valido (CN)                               | 0x1000 |
| La data o il certificato non è scaduto                    | 0x2000 |



 

Il valore predefinito di questa opzione nella versione 5,1 di WinHTTP è zero e pertanto non viene ignorato alcun errore. Nelle versioni precedenti di WinHTTP, l'impostazione predefinita era 0x3300, pertanto tutti gli errori del certificato del server venivano ignorati per impostazione predefinita.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**\_SelectCertificate WinHttpRequestOption**
</dt> <dd>

Imposta un **Variant** che specifica il certificato client inviato a un server per l'autenticazione. Questa opzione indica il percorso, l' [*archivio certificati*](glossary.md)e l'oggetto di un certificato client delimitato da barre rovesciate. Per ulteriori informazioni sulla selezione di un certificato client, vedere [SSL in WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**\_EnableRedirects WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica se le richieste vengono reindirizzate automaticamente quando il server specifica un nuovo percorso per la risorsa. Il valore predefinito di questa opzione è **Variant \_ true** per indicare che le richieste vengono reindirizzate automaticamente.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**\_UrlEscapeDisable WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica se i caratteri unsafe nel percorso e i componenti della query di un URL vengono convertiti in sequenze di escape. Il valore predefinito di questa opzione è **Variant \_ true**, che specifica che i caratteri nel percorso e nella query vengono convertiti.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**\_UrlEscapeDisableQuery WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica se i caratteri unsafe nel componente di query dell'URL vengono convertiti in sequenze di escape. Il valore predefinito di questa opzione è **Variant \_ true**, che specifica che i caratteri nella query vengono convertiti.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**\_SecureProtocols WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un **Variant** che indica i protocolli protetti che è possibile utilizzare. Questa opzione consente di selezionare i protocolli accettabili per il client. Il protocollo viene negoziato durante l'handshake di Secure Sockets Layer (SSL). Può trattarsi di una combinazione di uno o più dei flag seguenti.



| Protocollo                           | Valore  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Transport Layer Security (TLS) 1,0 | 0x0080 |



 

Il valore predefinito di questa opzione è 0x0028, che indica che è possibile utilizzare SSL 2,0 o SSL 3,0. Se questa opzione è impostata su zero, il client e il server non sono in grado di determinare un protocollo di sicurezza accettabile e l' [**invio**](iwinhttprequest-send.md) successivo genera un errore.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**\_EnableTracing WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un valore **Variant** che indica se la traccia è attualmente abilitata. Per ulteriori informazioni sulla funzionalità di traccia in servizi HTTP di Microsoft Windows (WinHTTP), vedere la pagina relativa alla [funzionalità di traccia WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**\_RevertImpersonationOverSsl WinHttpRequestOption**
</dt> <dd>

Controlla se l'oggetto [**WinHttpRequest**](winhttprequest.md) Annulla temporaneamente la rappresentazione client per la durata delle operazioni di autenticazione del certificato SSL. L'impostazione predefinita per l'oggetto **WinHttpRequest** è **true**. Impostare questa opzione su **false** per evitare la rappresentazione durante l'esecuzione delle operazioni di autenticazione del certificato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**\_EnableHttpsToHttpRedirects WinHttpRequestOption**
</dt> <dd>

Controlla se WinHTTP consente i reindirizzamenti. Per impostazione predefinita, tutti i reindirizzamenti vengono seguiti automaticamente, ad eccezione di quelli che trasferiscono da un URL protetto (HTTPS) a un URL non protetto (http). Impostare questa opzione su **true** per abilitare i reindirizzamenti HTTPS ai reindirizzamenti HTTP.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**\_EnablePassportAuthentication WinHttpRequestOption**
</dt> <dd>

Abilita o Disabilita il supporto per l'autenticazione Passport. Per impostazione predefinita, il supporto automatico per l'autenticazione Passport è disabilitato; impostare questa opzione su **true** per abilitare il supporto per l'autenticazione Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**\_MaxAutomaticRedirects WinHttpRequestOption**
</dt> <dd>

Imposta o Recupera il numero massimo di reindirizzamenti che WinHTTP segue; il valore predefinito è 10. Questo limite impedisce ai siti non autorizzati di rendere il client WinHTTP bloccato in seguito a un numero elevato di reindirizzamenti.

**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**\_MaxResponseHeaderSize WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un set associato sulla dimensione massima della parte di intestazione della risposta del server. Questo limite protegge il client da un server dannoso che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione. Il valore predefinito è 64 KB.

**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**\_MaxResponseDrainSize WinHttpRequestOption**
</dt> <dd>

Imposta o recupera un limite sulla quantità di dati che verranno svuotati dalle risposte per riutilizzare una connessione. Il valore predefinito è 1 MB.

**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Imposta o recupera un valore booleano che indica se è necessario utilizzare HTTP/1.1 o HTTP/1.0. Il valore predefinito è **true**, in modo che http/1.1 venga usato per impostazione predefinita.

**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**\_EnableCertificateRevocationCheck WinHttpRequestOption**
</dt> <dd>

Abilita il controllo delle revoche di certificati del server durante la negoziazione SSL. Quando il server presenta un certificato, viene eseguito un controllo per determinare se il certificato è stato revocato dall'emittente. Se il certificato è stato effettivamente revocato oppure il controllo della revoca non riesce perché non è possibile scaricare l'elenco di revoche di certificati (CRL), la richiesta ha esito negativo. questi errori di revoca non possono essere eliminati.

**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Impostare un'opzione specificando una delle costanti precedenti come parametro della proprietà [**Option**](iwinhttprequest-option.md) .

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




