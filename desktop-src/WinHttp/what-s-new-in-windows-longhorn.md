---
description: A partire da Windows Server 2008 e Windows Vista, l'API WinHTTP è stata migliorata per includere le funzionalità seguenti.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Novità di Windows Server 2008 e Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484996"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Novità di Windows Server 2008 e Windows Vista

A partire da Windows Server 2008 e Windows Vista, l'API WinHTTP è stata migliorata per includere le funzionalità seguenti.

## <a name="greater-than-4-gb-upload"></a>Maggiore di 4 GB di caricamento.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) può inviare solo 4 GB di dati a causa delle limitazioni della dimensione del parametro della lunghezza totale DWORD. Per consentire alle applicazioni di inviare più di 4 GB di dati, l'intestazione Content-Length viene aggiunta alla richiesta specificando i dati di grandi dimensioni come un \_ numero intero grande (2 ^ 64 byte). Per ulteriori informazioni, vedere **WinHttpSendRequest**. Questa funzionalità non è supportata nell'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="transfer-encoding-header"></a>Intestazione Transfer-Encoding

L'intestazione Transfer-Encoding consente alle applicazioni di inviare dati in blocchi al server. Quando l'intestazione Transfer-Encoding è presente nella richiesta, l'applicazione invia la richiesta con il corpo dell'entità di lunghezza zero nella chiamata a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Il corpo dell'entità viene inviato in chiamate successive a [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Questa funzionalità non è supportata nell'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recupero dell'elenco di autorità emittenti del certificato client SSL

L'applicazione può recuperare l'elenco di autorità emittenti del certificato client SSL quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha esito negativo con un errore di certificato di **\_ \_ autenticazione client WinHTTP \_ \_ \_ necessario**. Una nuova opzione, **WinHTTP \_ option \_ client certificate \_ \_ Issuer \_ List**, consente alle applicazioni di recuperare l'elenco di autorità di certificazione e filtrare l'elenco per il certificato ottimale. Per ulteriori informazioni, vedere gli argomenti relativi a [**flag di opzione**](option-flags.md) e [recupero di elenchi di autorità emittenti per l'autenticazione client SSL](ssl-in-winhttp.md) . Questa funzionalità non è supportata nell'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="optional-client-certificates"></a>Certificati client facoltativi

Quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha esito negativo con un errore del certificato di **\_ autenticazione del \_ client WinHTTP \_ \_ \_ necessario**, il server potrebbe non richiedere il certificato client SSL. Il server potrebbe essere in grado di ripristinare un'altra forma di autenticazione oppure consentire al client di procedere con l'accesso anonimo. L'applicazione imposta l'opzione del contesto del certificato **\_ client dell'opzione \_ \_ \_ WinHTTP** e specifica una macro utilizzata da WinHTTP per determinare se il certificato client è obbligatorio. Per ulteriori informazioni, vedere [**flag di opzione**](option-flags.md). Questa funzionalità non è supportata nell'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="source-and-destination-ip-addresses"></a>Indirizzi IP di origine e di destinazione

Al termine dell'esecuzione di [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , l'applicazione può recuperare l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta. Viene fornita una nuova struttura per ricevere gli indirizzi di origine e di destinazione quando è impostata l'opzione per le **\_ informazioni di \_ connessione \_ dell'opzione WinHTTP** . Per ulteriori informazioni, vedere [**flag di opzione**](option-flags.md). Questa funzionalità non è supportata nell'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="additional-ssl-client-authentication-errors"></a>Errori di autenticazione client SSL aggiuntivi

Altri errori di autenticazione client SSL forniscono ulteriori informazioni sul certificato client SSL. **Errore \_ Certificato \_ client \_ WinHTTP \_ Nessuna \_ \_ chiave privata** ed **errore \_ certificato \_ WinHTTP \_ nessun \_ accesso \_ \_ chiave privata** errori certificato client sono una novità per Windows Server 2008 e Windows Vista. L'oggetto com [**IWinHttpRequest**](iwinhttprequest-interface.md) restituisce questi errori in un valore HRESULT.

 

 



