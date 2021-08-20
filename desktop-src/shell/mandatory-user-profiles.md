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
ms.openlocfilehash: 748135affd0b6be399242ff171c88a45da3047911f0603f47eccf0a1f0ba0018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678145"
---
# <a name="mandatory-user-profiles"></a>Profili utente obbligatori

Un profilo utente obbligatorio è un tipo speciale di profilo utente [mobile](roaming-user-profiles.md) preconfigurato che gli amministratori possono usare per specificare le impostazioni per gli utenti. Con i profili utente obbligatori, un utente può modificare il proprio desktop, ma le modifiche non vengono salvate quando l'utente si disconnette. Al successivo accesso dell'utente, viene scaricato il profilo utente obbligatorio creato dall'amministratore. Esistono due tipi di profili obbligatori: *normali profili obbligatori* e profili super *obbligatori.*

I profili utente diventano profili obbligatori quando l'amministratore rinomina il file NTuser.dat (hive del Registro di sistema) nel server in NTuser.man. L'estensione .man fa sì che il profilo utente sia un profilo di sola lettura.

I profili utente *diventano super obbligatori* quando il nome della cartella del percorso del profilo termina con .man; ad esempio, \\ \\ condivisione server \\ \\ mandatoryprofile.man \\ .

I profili utente super obbligatori sono simili ai normali profili obbligatori, ad eccezione del fatto che gli utenti con profili super obbligatori non possono accedere quando il server in cui è archiviato il profilo obbligatorio non è disponibile. Gli utenti con profili obbligatori normali possono accedere con la copia memorizzata nella cache locale del profilo obbligatorio.

Solo gli amministratori di sistema possono apportare modifiche ai profili utente obbligatori.

 

 



