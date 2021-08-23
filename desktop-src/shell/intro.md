---
description: L Windows interno dell'interfaccia utente offre agli utenti l'accesso a un'ampia gamma di oggetti necessari per eseguire applicazioni e gestire il sistema operativo.
title: Guida per gli sviluppatori della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e6fbef1a8e34746d3b430faa5cb03f93613bc7c35e047cdd35afeb4921a37fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032299"
---
# <a name="shell-developers-guide"></a>Guida per gli sviluppatori della shell

L Windows interno dell'interfaccia utente offre agli utenti l'accesso a un'ampia gamma di oggetti necessari per eseguire applicazioni e gestire il sistema operativo. I più numerosi e familiari di questi oggetti sono le cartelle e i file che si trovano nelle unità disco del computer. Sono inoltre disponibili diversi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file a stampanti remote o l'accesso al Cestino. La shell organizza questi oggetti in uno spazio dei nomi gerarchico e offre a utenti e applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Considerazioni sulla sicurezza: Microsoft Windows Shell](sec-shell.md)
-   [Linee guida per l'implementazione In-Process estensioni](shell-and-managed-code.md)
-   [Versioni della shell e dei controlli comuni](versions.md)
-   [Implementazione delle interfacce dell'oggetto cartella di base](nse-implement.md)
-   [Implementazione di un formato di file personalizzato](customizing-file-types-bumper.md)
-   [Estendibilità della shell (creazione di un'origine dati)](shell-extensibility-bumper.md)
-   [Implementazione di Pannello di controllo elementi](control-panel-applications.md)
-   [Supporto delle applicazioni shell](application-support-bumper.md)
-   [Argomenti relativi alla shell legacy](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenzioni dei documenti

La Shell Developers's Guide (Guida per gli sviluppatori shell) segue le Windows standard del documento Software Development Kit (SDK). In particolare, è necessario prendere in particolare presente due convenzioni:

-   Il codice di esempio omette il normale codice di correzione degli errori. Questo codice è stato rimosso solo per rendere il codice più leggibile. È consigliabile includere tutto il codice di correzione degli errori appropriato nelle proprie applicazioni.
-   Per cancellare le voci del Registro di sistema di esempio, i nomi di chiave, sottochiave e voce, nonché i valori vengono visualizzati con un tipo di carattere standard. I nomi degli elementi definiti dall'utente o dall'applicazione sono in corsivo.

 

 



