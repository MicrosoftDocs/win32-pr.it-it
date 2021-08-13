---
description: Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: Metodo IWinHttpRequest::SetClientCertificate
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
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562897"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Metodo IWinHttpRequest::SetClientCertificate

Il **metodo SetClientCertificate** seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientCertificate* \[ Pollici\]
</dt> <dd>

Specifica il percorso, [*l'archivio certificati*](glossary.md)e l'oggetto di un certificato client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

La stringa specificata nel *parametro ClientCertificate* è costituita dal percorso del certificato, dall'archivio certificati e dal nome del soggetto delimitati da barre rovesciate. Per altre informazioni sui componenti della stringa del certificato, vedere [Certificati client.](ssl-in-winhttp.md)

Il nome e il percorso dell'archivio certificati sono facoltativi. Tuttavia, se si specifica un archivio certificati, è necessario specificare anche il percorso di tale archivio certificati. Il percorso predefinito è CURRENT \_ USER e l'archivio certificati predefinito è "MY". Un oggetto vuoto indica che deve essere usato il primo certificato nell'archivio certificati.

Chiamare **SetClientCertificate per** selezionare un certificato prima di chiamare [**Send**](iwinhttprequest-send.md) per inviare la richiesta.

Microsoft Windows servizi HTTP (WinHTTP) non fornisce certificati client ai server proxy che richiedono certificati per l'autenticazione.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la [sezione Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio di scripting seguente viene illustrato come selezionare un certificato client da inviare con una richiesta. Un certificato con oggetto "My Middle-Tier Certificate" viene scelto dall'archivio certificati "Personale" nel Registro di sistema in **HKEY \_ LOCAL \_ MACHINE**. Poiché questo esempio di codice è specifico di Microsoft JScript, che usa la barra rovesciata come carattere di escape, sono necessarie due barre rovesciate adiacenti per delimitare i componenti della stringa del certificato.


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
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SSL in WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




