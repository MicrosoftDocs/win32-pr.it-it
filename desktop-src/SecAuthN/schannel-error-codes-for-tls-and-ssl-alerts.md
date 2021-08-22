---
description: Schannel restituisce i messaggi di errore seguenti quando l'avviso corrispondente viene ricevuto dai protocolli Transport Layer Security (TLS) o Secure Sockets Layer (SSL).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Codici di errore Schannel per gli avvisi TLS e SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4819c39948a2baf5889734fe7e2c08c8d85cbd22868cc9fad8a33281d13a306c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918590"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Codici di errore Schannel per gli avvisi TLS e SSL

[*Schannel*](../secgloss/s-gly.md) restituisce i messaggi di errore seguenti quando l'avviso corrispondente viene ricevuto dai protocolli [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) [*o Secure Sockets Layer*](../secgloss/s-gly.md) (SSL). I messaggi di errore sono definiti in Winerror.h.



| Avviso TLS o SSL                                           | Codice errore Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| MESSAGGIO \_ IMPREVISTO DI AVVISO SSL3 \_ \_<br/> 10<br/>  | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| MAC \_ RECORD DI AVVISO \_ TLS1 \_ NON \_ ERTA<br/> 20<br/>     | MESSAGGIO \_ SEC E \_ \_ MODIFICATO<br/> 0x8009030F<br/>             |
| DECRITTOGRAFIA DEGLI AVVISI TLS1 \_ \_ NON \_ RIUSCITA<br/> 21<br/>   | ERRORE \_ DI \_ DECRITTOGRAFIA SEC E \_<br/> 0x80090330<br/>             |
| OVERFLOW DEI RECORD DI AVVISO TLS1 \_ \_ \_<br/> 22<br/>     | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| ERRORE DI \_ \_ DECOMPRESSIONE DEGLI AVVISI SSL3 \_<br/> 30<br/>  | MESSAGGIO \_ SEC E \_ \_ MODIFICATO<br/> 0x8009030F<br/>             |
| ERRORE DI \_ \_ HANDSHAKE DI AVVISO SSL3 \_<br/> 40<br/>   | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| CERTIFICATO DI \_ AVVISO TLS1 \_ NON \_ VALIDO<br/> 42<br/>     | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| CERTIFICATO \_ DI AVVISO TLS1 \_ NON \_ SUPPORTATO<br/> 43<br/>    | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| CERTIFICATO DI AVVISO TLS1 \_ \_ \_ REVOCATO<br/> 44<br/> | CRYPT \_ E \_ REVOKED<br/> 0x80092010<br/>                    |
| CERTIFICATO DI AVVISO TLS1 \_ \_ \_ SCADUTO<br/> 45<br/> | SEC \_ E \_ CERT \_ SCADUTO<br/> 0x80090328<br/>                |
| CERTIFICATO DI AVVISO TLS1 \_ \_ \_ SCONOSCIUTO<br/> 46<br/> | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| PARAMETRO AVVISO SSL3 \_ \_ NON \_ VALIDO<br/>                 | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| AUTORITÀ DI CERTIFICAZIONE \_ SCONOSCIUTA \_ AVVISO TLS1 \_<br/> 48<br/>          | SEC \_ E RADICE NON \_ \_ ATTENDIBILE<br/> 0x80090325<br/>              |
| ACCESSO AGLI \_ AVVISI TLS1 \_ \_ NEGATO<br/> 49<br/>       | SEC \_ E \_ LOGON \_ DENIED<br/> 0x8009030C<br/>                |
| ERRORE DI DECODIFICA AVVISO TLS1 \_ \_ \_<br/> 50<br/>        | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| ERRORE DI \_ DECRITTOGRAFIA \_ AVVISO TLS1 \_<br/> 51<br/>       | ERRORE \_ DI \_ DECRITTOGRAFIA SEC E \_<br/> 0x80090330<br/>             |
| RESTRIZIONE \_ DELL'ESPORTAZIONE \_ DEGLI AVVISI TLS1 \_<br/> 60<br/>  | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| VERSIONE \_ DEL PROTOCOLLO DI \_ AVVISO \_ TLS1<br/> 70<br/>    | SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA<br/> 0x80090302<br/>        |
| SICUREZZA \_ DELL'AVVISO TLS1 \_ INSUFFIENT \_<br/> 71<br/> | MANCATA \_ CORRISPONDENZA \_ \_ DELL'ALGORITMO SEC E<br/> 0x80090331<br/>          |
| ERRORE INTERNO \_ DELL'AVVISO TLS1 \_ \_<br/> 80<br/>      | SEC \_ E \_ ERRORE \_ INTERNO<br/> 0x80090304<br/>              |
| UTENTE AVVISO TLS1 \_ \_ \_ ANNULLATO<br/> 90<br/>       | SEC \_ E \_ UNFINISHED \_ CONTEXT \_ DELETED<br/> 0x80090333<br/> |
| AVVISO \_ TLS1 \_ NESSUNA \_ RINEGOZIAZIONE<br/> 100<br/>   | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| TLS1 \_ ALERT \_ UNSUPPORTED \_ EXT<br/> 110<br/>    | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |
| Predefinito<br/>                                         | SEC \_ E MESSAGGIO NON \_ \_ VALIDO<br/> 0x80090326<br/>             |



 

 

 
