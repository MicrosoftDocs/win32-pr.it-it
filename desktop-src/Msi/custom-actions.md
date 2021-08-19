---
description: Il Windows di installazione offre molte azioni incorporate per l'esecuzione del processo di installazione. Per un elenco di queste azioni, vedere le informazioni di riferimento per le azioni standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3e2eb466934d7d332307e0d5288d6d328297d7664d884e62c406eb3409728a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947902"
---
# <a name="custom-actions"></a>Azioni personalizzate

Il Windows di installazione offre molte azioni incorporate per l'esecuzione del processo di installazione. Per un elenco di queste azioni, vedere le informazioni [di riferimento per le azioni standard.](standard-actions-reference.md)

Le azioni standard sono sufficienti per eseguire un'installazione nella maggior parte dei casi. In alcune situazioni, tuttavia, lo sviluppatore di un pacchetto di installazione rileva la necessità di scrivere un'azione personalizzata. Esempio:

-   Si vuole avviare un file eseguibile durante l'installazione che viene installato nel computer dell'utente o che viene installato con l'applicazione.
-   Si desidera chiamare funzioni speciali durante un'installazione definite in una libreria a collegamento dinamico (DLL).
-   Si vogliono usare funzioni scritte nei linguaggi di sviluppo Microsoft Visual Basic Scripting Edition o Microsoft JScript testo dello script letterale durante un'installazione.
-   Si desidera posticipare l'esecuzione di alcune azioni fino al momento in cui viene eseguito lo script di installazione.
-   Si vogliono aggiungere informazioni sull'ora e sullo stato a un controllo ProgressBar e a un controllo TimeRemaining Text.

Le sezioni seguenti descrivono le azioni personalizzate e come incorporarle in un pacchetto di installazione:

-   [Informazioni sulle azioni personalizzate](about-custom-actions.md)
-   [Uso di azioni personalizzate](using-custom-actions.md)
-   [Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
-   [Elenco di riepilogo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md)

 

 



