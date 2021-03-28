---
description: Un profilo utente obbligatorio è un tipo speciale di profilo utente mobile preconfigurato che gli amministratori possono usare per specificare le impostazioni per gli utenti.
title: Profili utente obbligatori
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524425"
---
# <a name="mandatory-user-profiles"></a>Profili utente obbligatori

Un profilo utente obbligatorio è un tipo speciale di [profilo utente mobile](roaming-user-profiles.md) preconfigurato che gli amministratori possono usare per specificare le impostazioni per gli utenti. Con i profili utente obbligatori, un utente può modificare il proprio desktop, ma le modifiche non vengono salvate quando l'utente si disconnette. Al successivo accesso dell'utente, verrà scaricato il profilo utente obbligatorio creato dall'amministratore. Esistono due tipi di profili obbligatori: i profili *obbligatori normali* e i profili *Super-obbligatori* .

I profili utente diventano profili obbligatori quando l'amministratore Rinomina il file NTuser. dat (hive del registro di sistema) nel server in NTuser. Man. L'estensione. Man fa in modo che il profilo utente sia un profilo di sola lettura.

I profili utente diventano *estremamente obbligatori* quando il nome della cartella del percorso del profilo termina con. Man; ad esempio, \\ \\ server \\ share \\ mandatoryprofile. man \\ .

I profili utente super-obbligatori sono simili ai normali profili obbligatori, ad eccezione del caso in cui gli utenti che dispongono di profili Super obbligatori non possano accedere quando il server in cui è archiviato il profilo obbligatorio non è disponibile. Gli utenti con profili obbligatori normali possono accedere con la copia memorizzata nella cache locale del profilo obbligatorio.

Solo gli amministratori di sistema possono apportare modifiche ai profili utente obbligatori.

 

 



