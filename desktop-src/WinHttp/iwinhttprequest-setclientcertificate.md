---
description: Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Metodo IWinHttpRequest:: SetClientCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347206"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Metodo IWinHttpRequest:: SetClientCertificate

Il metodo **SetClientCertificate** seleziona un certificato client da inviare a un server Secure HYPERTEXT Transfer Protocol (HTTPS).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientCertificate* \[ in\]
</dt> <dd>

Specifica il percorso, l' [*archivio certificati*](glossary.md)e l'oggetto di un certificato client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

La stringa specificata nel parametro *ClientCertificate* è costituita dal percorso del certificato, dall'archivio certificati e dal nome soggetto delimitati da barre rovesciate. Per ulteriori informazioni sui componenti della stringa del certificato, vedere [Client Certificates](ssl-in-winhttp.md).

Il nome e il percorso dell'archivio certificati sono facoltativi. Tuttavia, se si specifica un archivio certificati, è necessario specificare anche il percorso dell'archivio certificati. Il percorso predefinito è l' \_ utente corrente e l'archivio certificati predefinito è "My". Un oggetto vuoto indica che deve essere utilizzato il primo certificato nell'archivio certificati.

Chiamare **SetClientCertificate** per selezionare un certificato prima di chiamare [**Send**](iwinhttprequest-send.md) per inviare la richiesta.

I servizi HTTP di Microsoft Windows (WinHTTP) non forniscono certificati client per i server proxy che richiedono certificati per l'autenticazione.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio di script seguente viene illustrato come selezionare un certificato client da inviare con una richiesta. Un certificato con l'oggetto "My Middle-Tier certificate" viene scelto dall'archivio certificati "personali" nel registro di sistema in **HKEY \_ Local \_ computer**. Poiché questo esempio di codice è specifico di Microsoft JScript, che usa la barra rovesciata come carattere di escape, sono necessarie due barre rovesciate adiacenti per delimitare i componenti della stringa del certificato.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SSL in WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




