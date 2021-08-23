---
description: Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione. Windows Il programma di installazione include molte azioni standard incorporate. Gli sviluppatori di pacchetti di installazione possono anche creare azioni personalizzate.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e95c3ab95a7bddc1f23dd38108b2cb10978ad5316da60397e6f3ba019a415ac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627621"
---
# <a name="standard-actions"></a>Azioni standard

Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione. Windows Il programma di installazione include molte azioni standard incorporate. Gli sviluppatori di pacchetti di installazione possono anche creare [azioni personalizzate.](custom-actions.md)

Esempi di azioni standard del programma di installazione includono:

-   [Azione CreateShortcuts](createshortcuts-action.md): gestisce la creazione di collegamenti ai file installati con l'applicazione corrente. Questa azione usa la [tabella Collegamento](shortcut-table.md) per i relativi dati.
-   [Azione InstallFiles](installfiles-action.md): copia i file selezionati dalla directory di origine alla directory di destinazione. Questa azione usa la [tabella File](file-table.md) per i relativi dati.
-   [Azione WriteRegistryValues](writeregistryvalues-action.md): imposta le informazioni del Registro di sistema richieste dall'applicazione nel Registro di sistema. Questa azione usa la [tabella Registro di sistema](registry-table.md) per i relativi dati.

Le sezioni seguenti illustrano le azioni standard.

-   [Informazioni sulle azioni standard](about-standard-actions.md)
-   [Uso di azioni standard](using-standard-actions.md)
-   [Informazioni di riferimento su Azioni standard](standard-actions-reference.md)

 

 



