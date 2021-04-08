---
description: Schannel restituisce i messaggi di errore seguenti quando viene ricevuto l'avviso corrispondente dai protocolli Transport Layer Security (TLS) o Secure Sockets Layer (SSL).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Codici di errore Schannel per gli avvisi TLS e SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fdba202e63d212fc85f0c02eb5ac9dc20db047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967387"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Codici di errore Schannel per gli avvisi TLS e SSL

[*Schannel*](../secgloss/s-gly.md) restituisce i messaggi di errore seguenti quando viene ricevuto l'avviso corrispondente dai protocolli [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) o [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL). I messaggi di errore sono definiti in Winerror. h.



| Avviso TLS o SSL                                           | Codice errore Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| \_Avviso SSL3 \_ messaggio imprevisto \_<br/> 10<br/>  | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| TLS1 \_ avviso \_ \_ record errato \_ Mac<br/> 20<br/>     | SEC \_ E \_ messaggio \_ modificato<br/> 0x8009030F<br/>             |
| \_Decrittografia avviso TLS1 \_ \_ non riuscita<br/> 21<br/>   | SEC \_ E \_ errore di decrittografia \_<br/> 0x80090330<br/>             |
| \_ \_ Overflow record di avviso TLS1 \_<br/> 22<br/>     | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| \_Errore di \_ decompressione dell'avviso SSL3 \_<br/> 30<br/>  | SEC \_ E \_ messaggio \_ modificato<br/> 0x8009030F<br/>             |
| \_ \_ Errore handshake avviso \_ SSL3<br/> 40<br/>   | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| Certificato di avviso TLS1 non \_ \_ valido \_<br/> 42<br/>     | SEC \_ E \_ certificato \_ sconosciuto<br/> 0x80090327<br/>                |
| Certificato di avviso TLS1 non \_ \_ supportato \_<br/> 43<br/>    | SEC \_ E \_ certificato \_ sconosciuto<br/> 0x80090327<br/>                |
| \_Certificato di avviso TLS1 \_ \_ revocato<br/> 44<br/> | CRYPT \_ E \_ revocata<br/> 0x80092010<br/>                    |
| \_Certificato di avviso TLS1 \_ \_ scaduto<br/> 45<br/> | SEC \_ E \_ certificato \_ scaduto<br/> 0x80090328<br/>                |
| \_Certificato di avviso TLS1 \_ \_ sconosciuto<br/> 46<br/> | SEC \_ E \_ certificato \_ sconosciuto<br/> 0x80090327<br/>                |
| \_Parametro avviso SSL3 non \_ valido \_<br/>                 | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| \_ \_ CA sconosciuta avviso \_ TLS1<br/> 48<br/>          | SEC \_ E \_ radice non attendibile \_<br/> 0x80090325<br/>              |
| \_Accesso agli avvisi di TLS1 \_ \_ negato<br/> 49<br/>       | SEC \_ E \_ accesso \_ negato<br/> : 0X8009030c<br/>                |
| \_Errore di \_ decodifica dell'avviso TLS1 \_<br/> 50<br/>        | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| \_Errore di \_ decrittografia dell'avviso TLS1 \_<br/> 51<br/>       | SEC \_ E \_ errore di decrittografia \_<br/> 0x80090330<br/>             |
| \_ \_ Restrizione esportazione avvisi TLS1 \_<br/> 60<br/>  | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| \_Versione del \_ protocollo di avviso TLS1 \_<br/> 70<br/>    | SEC \_ E \_ funzione non supportata \_<br/> 0x80090302<br/>        |
| \_ \_ Sicurezza INSUFFIENT avviso \_ TLS1<br/> 71<br/> | SEC \_ E \_ algoritmo non \_ corrispondenti<br/> 0x80090331<br/>          |
| \_ \_ Errore interno avviso \_ TLS1<br/> 80<br/>      | \_ \_ errore interno sec \_ E<br/> 0x80090304<br/>              |
| \_Utente avviso \_ TLS1 \_ annullato<br/> 90<br/>       | SEC \_ E \_ contesto non completato \_ \_ eliminato<br/> 0x80090333<br/> |
| Avviso di TLS1 \_ \_ senza \_ rinegoziazione<br/> 100<br/>   | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| Avviso di TLS1 non \_ \_ supportato da \_ ext<br/> 110<br/>    | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |
| Predefinito<br/>                                         | SEC \_ E \_ messaggio non valido \_<br/> 0x80090326<br/>             |



 

 

 
