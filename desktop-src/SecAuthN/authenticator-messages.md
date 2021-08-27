---
description: In un protocollo semplice che usa l'autenticazione con chiave privata, un client presenta un messaggio dell'autenticatore sotto forma di informazioni crittografate nella chiave di sessione.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Authenticator Messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc21cd87fbf1b725f276f138bcd0bd513658428ddd1296c4016542953bd8b86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035461"
---
# <a name="authenticator-messages"></a>Authenticator Messaggi

In un protocollo semplice che usa l'autenticazione con chiave privata, un client presenta un messaggio dell'autenticatore sotto forma di informazioni crittografate nella [*chiave di sessione*](/windows/desktop/SecGloss/s-gly). Le informazioni nel messaggio dell'autenticatore devono essere diverse ogni volta che viene eseguito il protocollo di autenticazione oppure un messaggio crittografato dell'autenticatore può essere riutilizzato da un'entità non autorizzata.

Alla ricezione del messaggio dell'autenticatore, il server lo decrittografa e può indicare dal contenuto del messaggio decrittografato se la decrittografia è riuscita. Se il messaggio decrittografato non è incompleto, il server sa che il client che presenta il messaggio dell'autenticatore ha usato la chiave corretta per crittografare il messaggio. Solo due entità hanno [](/windows/desktop/SecGloss/s-gly) accesso alla chiave di sessione e, se il server è una di queste, il client che ha crittografato il messaggio dell'autenticatore deve essere l'altra.

Per l'autenticazione reciproca, viene eseguito un protocollo simile. Il server estrae parte delle informazioni dal messaggio di autenticazione originale decrittografato, le crittografa con la chiave di sessione condivisa e invia il messaggio crittografato al client. Il client decrittografa il messaggio e confronta il risultato con l'originale. Se il messaggio decrittografato corrisponde alla parte corretta del messaggio originale, il client sa che il server è stato in grado di decrittografare il messaggio originale con la chiave di sessione privata condivisa ed è stato in grado di crittografare nuovamente una parte del messaggio con la stessa chiave di sessione privata [*condivisa*](/windows/desktop/SecGloss/s-gly).

 

 
