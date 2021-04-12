---
description: Per garantire la protezione di un'installazione software, attenersi a queste linee guida durante la creazione di un Windows Installer azione personalizzata.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Linee guida per la protezione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232253"
---
# <a name="guidelines-for-securing-custom-actions"></a>Linee guida per la protezione di azioni personalizzate

La conformità alle linee guida seguenti quando si crea un pacchetto di Windows Installer con azioni personalizzate consente di mantenere un ambiente protetto durante l'installazione:

-   Proteggere tutti i file aggiuntivi scritti dall'azione personalizzata.
-   Controllare le lunghezze del buffer e la validità di tutti i dati letti dall'azione personalizzata. Sono incluse le proprietà che possono fornire dati all'azione personalizzata, in particolare quelle che utilizzano proprietà pubbliche fornite da un utente.
-   Non fare affidamento su dll esterne non ritenuti attendibili dal sistema in tutte le piattaforme in cui è previsto l'esecuzione del pacchetto di installazione.
-   Valutare attentamente se usare azioni personalizzate che usano privilegi [*elevati*](e-gly.md) o la rappresentazione. Azioni personalizzate, ad esempio "apertura di un URL dopo il completamento dell'installazione", "avvio del software dopo il completamento dell'installazione" o "avvio del file Leggimi al termine dell'installazione" non richiede in genere privilegi elevati per funzionare. Se l'azione personalizzata deve essere eseguita con privilegi *elevati* , assicurarsi che il codice dell'azione personalizzata protegga dai sovraccarichi del buffer e dal caricamento accidentale del codice unsafe. Si noti che durante la fase di esecuzione dell'installazione, il programma di installazione passa informazioni a un processo con privilegi *elevati* ed esegue lo script. Qualsiasi azione personalizzata eseguita durante la fase di esecuzione può essere eseguita con privilegi *elevati* .
-   Consente di raccogliere tutte le informazioni fornite dall'utente durante la sequenza dell'interfaccia utente. Non richiedere all'utente le informazioni che non possono essere impostate con una proprietà pubblica.
-   Se l'azione personalizzata dello script espande le proprietà, adottare le precauzioni per garantire che l'azione personalizzata sia protetta dalla possibilità di inserimento di script. È possibile che lo script venga registrato come testo non crittografato.

Vedere anche [sicurezza dell'azione personalizzata](custom-action-security.md).

 

 



