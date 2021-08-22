---
description: Per garantire la sicurezza di un'installazione del software, attenersi a queste linee guida quando si crea un'Windows personalizzata del programma di installazione.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Linee guida per la protezione delle azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b5ea12bd8d38025587cb09fd7a17d3e87739acedf31d85f72ff4b1b76b0432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649291"
---
# <a name="guidelines-for-securing-custom-actions"></a>Linee guida per la protezione delle azioni personalizzate

L'aderenza alle linee guida seguenti quando si crea un pacchetto Windows installer con azioni personalizzate consente di mantenere un ambiente sicuro durante l'installazione:

-   Proteggere eventuali file aggiuntivi scritti dall'azione personalizzata.
-   Controllare la lunghezza del buffer e la validità di tutti i dati letti dall'azione personalizzata. Sono incluse le proprietà che possono fornire dati all'azione personalizzata, in particolare quelle che usano proprietà pubbliche fornite da un utente.
-   Non basarsi su DLL esterne non attendibili dal sistema in tutte le piattaforme in cui il pacchetto di installazione deve essere eseguito.
-   Valutare attentamente se usare azioni personalizzate che usano [*privilegi*](e-gly.md) elevati o la rappresentazione. Azioni personalizzate, ad esempio "apri un URL al termine dell'installazione", "avvia il software al termine dell'installazione" o "avvia ReadMe al termine dell'installazione" non richiede in genere privilegi elevati per funzionare. Se l'azione personalizzata  deve essere eseguita con privilegi elevati, assicurarsi che il codice dell'azione personalizzata protegge dai sovraccarichi del buffer e dal caricamento accidentale di codice non sicuro. Si noti che durante la fase di esecuzione dell'installazione, il programma di installazione passa le informazioni a un processo con privilegi elevati ed esegue lo script.  Qualsiasi azione personalizzata eseguita durante la fase di esecuzione può essere eseguita con *privilegi* elevati.
-   Raccogliere tutte le informazioni fornite dall'utente durante la sequenza dell'interfaccia utente. Non richiedere all'utente informazioni che non possono essere impostate usando una proprietà pubblica.
-   Se l'azione personalizzata dello script espande le proprietà, prendere le precauzioni necessarie perché l'azione personalizzata sia protetta dalla possibilità di inserimento di script. Lo script può essere registrato in testo non crittografato.

Vedere anche [Sicurezza delle azioni personalizzate.](custom-action-security.md)

 

 



