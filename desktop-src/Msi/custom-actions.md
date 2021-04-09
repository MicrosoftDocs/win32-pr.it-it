---
description: Il Windows Installer fornisce molte azioni predefinite per l'esecuzione del processo di installazione. Per un elenco di queste azioni, vedere le informazioni di riferimento sulle azioni standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050152"
---
# <a name="custom-actions"></a>Azioni personalizzate

Il Windows Installer fornisce molte azioni predefinite per l'esecuzione del processo di installazione. Per un elenco di queste azioni, vedere le informazioni di [riferimento sulle azioni standard](standard-actions-reference.md).

Le azioni standard sono sufficienti per eseguire un'installazione nella maggior parte dei casi. Tuttavia, esistono situazioni in cui lo sviluppatore di un pacchetto di installazione rileva che è necessario scrivere un'azione personalizzata. Ad esempio:

-   Si vuole avviare un file eseguibile durante l'installazione installato nel computer dell'utente o installato con l'applicazione.
-   Si desidera chiamare funzioni speciali durante un'installazione definita in una libreria a collegamento dinamico (DLL).
-   Si desidera utilizzare le funzioni scritte nei linguaggi di sviluppo Microsoft Visual Basic Scripting Edition o testo script letterale di Microsoft JScript durante un'installazione.
-   Si desidera rinviare l'esecuzione di alcune azioni fino al momento in cui viene eseguito lo script di installazione.
-   Si desidera aggiungere informazioni sull'ora e sullo stato di avanzamento a un controllo ProgressBar e a un controllo di testo TimeRemaining.

Nelle sezioni seguenti vengono descritte le azioni personalizzate e le modalità di incorporamento in un pacchetto di installazione:

-   [Informazioni sulle azioni personalizzate](about-custom-actions.md)
-   [Uso di azioni personalizzate](using-custom-actions.md)
-   [Riferimento all'azione personalizzata](custom-action-reference.md)
-   [Elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md)

 

 



