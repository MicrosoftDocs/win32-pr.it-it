---
description: L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per eseguire le applicazioni e gestire il sistema operativo.
title: Guida per gli sviluppatori della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993853"
---
# <a name="shell-developers-guide"></a>Guida per gli sviluppatori della shell

L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per eseguire le applicazioni e gestire il sistema operativo. I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer. Sono inoltre disponibili numerosi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file alle stampanti remote o l'accesso al Cestino. La shell organizza questi oggetti in uno spazio dei nomi gerarchico e fornisce agli utenti e alle applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Considerazioni sulla sicurezza: shell Microsoft Windows](sec-shell.md)
-   [Linee guida per l'implementazione di estensioni In-Process](shell-and-managed-code.md)
-   [Versioni di Shell e controlli comuni](versions.md)
-   [Implementazione delle interfacce di oggetti della cartella di base](nse-implement.md)
-   [Implementazione di un formato di file personalizzato](customizing-file-types-bumper.md)
-   [Estendibilità della shell (creazione di un'origine dati)](shell-extensibility-bumper.md)
-   [Implementazione degli elementi del pannello di controllo](control-panel-applications.md)
-   [Supporto delle applicazioni shell](application-support-bumper.md)
-   [Argomenti della shell legacy](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenzioni documento

La guida per gli sviluppatori della shell segue le normali convenzioni dei documenti Windows Software Development Kit (SDK). Si noti che in particolare è necessario tenere presente due convenzioni:

-   Il codice di esempio omette il normale codice di correzione degli errori. Questo codice è stato rimosso solo per rendere il codice più leggibile. È necessario includere tutto il codice di correzione degli errori appropriato nelle proprie applicazioni.
-   Per rendere evidenti le voci del registro di sistema, la chiave, la sottochiave e i nomi di voce, nonché i valori, vengono visualizzati con un tipo di carattere standard. I nomi degli elementi definiti dall'utente o dall'applicazione sono in corsivo.

 

 



