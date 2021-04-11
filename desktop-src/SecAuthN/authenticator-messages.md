---
description: In un protocollo semplice che usa l'autenticazione con chiave privata, un client presenta un messaggio di autenticatore sotto forma di informazioni crittografate nella chiave della sessione.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Messaggi di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232044"
---
# <a name="authenticator-messages"></a>Messaggi di autenticazione

In un protocollo semplice che usa l'autenticazione con chiave privata, un client presenta un messaggio di autenticatore sotto forma di informazioni crittografate nella [*chiave della sessione*](/windows/desktop/SecGloss/s-gly). Le informazioni nel messaggio dell'autenticatore devono essere diverse ogni volta che viene eseguito il protocollo di autenticazione oppure è possibile riutilizzare un messaggio autenticatore crittografato da un'entità non autorizzata.

Alla ricezione del messaggio di autenticazione, il server lo decrittografa e può distinguere dal contenuto del messaggio decrittografato se la decrittografia ha avuto esito positivo. Se il messaggio decrittografato non è incomprensibile, il server sa che il client che presenta il messaggio di autenticazione ha utilizzato la chiave corretta per crittografare il messaggio. Solo due entità hanno accesso alla [*chiave di sessione*](/windows/desktop/SecGloss/s-gly) e se il server è uno di questi, il client che ha crittografato il messaggio di autenticazione deve essere l'altro.

Per l'autenticazione reciproca, viene eseguito un protocollo simile. Il server estrae parte delle informazioni dal messaggio di autenticazione originale decrittografato, lo crittografa con la chiave della sessione condivisa e invia il messaggio crittografato al client. Il client decrittografa il messaggio e confronta il risultato con quello originale. Se il messaggio decrittografato corrisponde alla parte corretta del messaggio originale, il client sa che il server è stato in grado di decrittografare il messaggio originale con la chiave della sessione segreta condivisa ed è stato in grado di crittografare nuovamente una parte del messaggio con la stessa [*chiave di sessione*](/windows/desktop/SecGloss/s-gly)segreta condivisa.

 

 
