---
description: A partire da Windows Server 2008 e Windows Vista, l'API WinHTTP è stata migliorata per includere le funzionalità seguenti.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Novità di Windows Server 2008 e Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e474bbfa32d8f82737df4be6f537ca0a6f1bc870e2028d7dcdb1f418adb7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071701"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Novità di Windows Server 2008 e Windows Vista

A partire da Windows Server 2008 e Windows Vista, l'API WinHTTP è stata migliorata per includere le funzionalità seguenti.

## <a name="greater-than-4-gb-upload"></a>Maggiore di 4 GB Upload.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) può inviare solo 4 GB di dati a causa di limitazioni nelle dimensioni del parametro di lunghezza totale DWORD. Per consentire alle applicazioni di inviare più di 4 GB di dati, l'intestazione Content-Length viene aggiunta alla richiesta specificando dati grandi come LARGE \_ INTEGER (2^64 byte). Per altre informazioni, vedere **WinHttpSendRequest.** Questa funzionalità non è supportata nell'oggetto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="transfer-encoding-header"></a>Transfer-Encoding intestazione

LTransfer-Encoding invio consente alle applicazioni di inviare dati in blocchi al server. Quando lTransfer-Encoding a header è presente nella richiesta, l'applicazione invia la richiesta con un corpo di entità di lunghezza zero nella chiamata a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Il corpo dell'entità viene inviato nelle chiamate successive [**a WinHttpWriteData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) Questa funzionalità non è supportata nell'oggetto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recupero elenco autorità di certificazione del certificato client SSL

L'applicazione può recuperare l'elenco autorità di certificazione del certificato client SSL quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha esito negativo con **errore \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED**. Una nuova opzione, **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST,** consente alle applicazioni di recuperare l'elenco di autorità di certificazione del certificato e filtrare l'elenco per il certificato ottimale. Per altre informazioni, vedere gli argomenti [**Flag di opzione**](option-flags.md) e Recupero dell'elenco di autorità di emissione per [l'autenticazione client SSL.](ssl-in-winhttp.md) Questa funzionalità non è supportata nell'oggetto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="optional-client-certificates"></a>Certificati client facoltativi

Quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha esito negativo con **errore \_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED**, il server potrebbe non richiedere il certificato client SSL. Il server può essere in grado di ripristinare un'altra forma di autenticazione o consentire al client di procedere con l'accesso anonimo. L'applicazione imposta **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** e specifica una macro che WinHttp usa per determinare se il certificato client è obbligatorio. Per altre informazioni, vedere [**Flag di opzione**](option-flags.md). Questa funzionalità non è supportata nell'oggetto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="source-and-destination-ip-addresses"></a>Indirizzi IP di origine e di destinazione

Al [**termine di WinHttpReceiveResponse,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) l'applicazione può recuperare l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta. Viene fornita una nuova struttura per ricevere gli indirizzi di origine e di destinazione quando è impostata l'opzione **WINHTTP \_ OPTION CONNECTION \_ \_ INFO.** Per altre informazioni, vedere [**Flag di opzione**](option-flags.md). Questa funzionalità non è supportata nell'oggetto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="additional-ssl-client-authentication-errors"></a>Altri errori di autenticazione client SSL

Altri errori di autenticazione client SSL forniscono altre informazioni sul certificato client SSL. **ERRORE \_ Gli errori del certificato client WINHTTP \_ CLIENT \_ CERT \_ NO PRIVATE \_ \_ KEY** e **ERROR \_ WINHTTP \_ CERT NO ACCESS PRIVATE \_ \_ \_ \_ KEY** sono nuovi per Windows Server 2008 e Windows Vista. L'oggetto COM [**IWinHttpRequest**](iwinhttprequest-interface.md) restituisce questi errori in un HRESULT.

 

 



