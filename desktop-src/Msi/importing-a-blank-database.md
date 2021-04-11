---
description: Per riprodurre l'esempio è necessario copiare o creare con uno strumento software, un file di database Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importazione di un database vuoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232442"
---
# <a name="importing-a-blank-database"></a>Importazione di un database vuoto

Per riprodurre l'esempio è necessario copiare o creare con uno strumento software, un file di database Windows Installer. Un database di installazione completamente vuoto, Schema.msi, viene fornito con i [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). L'SDK fornisce anche un database parzialmente vuoto, uisample.msi, che contiene le tabelle di sequenza suggerite e i dati necessari per una semplice interfaccia utente. Creare una copia di uisample.msi e spostarla nella stessa directory contenente la cartella del blocco note creata durante [la pianificazione dell'installazione](planning-the-installation.md). Rinominare il file MNP2000.msi. Il file di database di installazione e i file di origine devono trovarsi nella radice della stessa directory. Ad esempio:

C: \\MNP2000.msi di esempio \\

C: \\ \\ blocco note di esempio\\

Se non si usa Uisample.msi, è necessario ottenere un database vuoto, ad esempio Schema.msi, e immettere le informazioni per l'installazione usando uno strumento di modifica del database, ad esempio ORCA, fornito con l'SDK o un altro editor di database.

[Continua](specifying-directory-structure.md)

 

 



