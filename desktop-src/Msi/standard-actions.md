---
description: Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione. Windows Installer dispone di molte azioni standard predefinite. Gli sviluppatori di pacchetti di installazione possono anche creare azioni personalizzate.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227056"
---
# <a name="standard-actions"></a>Azioni standard

Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione. Windows Installer dispone di molte azioni standard predefinite. Gli sviluppatori di pacchetti di installazione possono anche creare [azioni personalizzate](custom-actions.md).

Esempi di azioni standard del programma di installazione includono:

-   [Azione CreateShortcuts](createshortcuts-action.md): gestisce la creazione di collegamenti ai file installati con l'applicazione corrente. Questa azione utilizza la [tabella dei collegamenti](shortcut-table.md) per i relativi dati.
-   [Azione InstallFiles](installfiles-action.md): copia i file selezionati dalla directory di origine alla directory di destinazione. Questa azione utilizza la [tabella file](file-table.md) per i relativi dati.
-   [Azione WriteRegistryValori consente](writeregistryvalues-action.md): configura le informazioni del registro di sistema richieste dall'applicazione nel registro di sistema. Questa azione utilizza la [tabella del registro di sistema](registry-table.md) per i relativi dati.

Le sezioni seguenti illustrano le azioni standard.

-   [Informazioni sulle azioni standard](about-standard-actions.md)
-   [Uso di azioni standard](using-standard-actions.md)
-   [Guida di riferimento alle azioni standard](standard-actions-reference.md)

 

 



