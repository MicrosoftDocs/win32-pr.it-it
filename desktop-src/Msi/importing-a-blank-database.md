---
description: Per riprodurre l'esempio è necessario copiare o creare con uno strumento software un file di database Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importazione di un database vuoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3d2c0a7b0fa8d6364a9eef66b830f94e3523c2dfece9c6e1ec459d146ace11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946598"
---
# <a name="importing-a-blank-database"></a>Importazione di un database vuoto

Per riprodurre l'esempio è necessario copiare o creare con uno strumento software un file di database Windows Installer. Un database di installazione completamente vuoto, Schema.msi, viene fornito con Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). L'SDK fornisce anche un database parzialmente vuoto, uisample.msi, che contiene le tabelle di sequenza suggerite e i dati necessari per una semplice interfaccia utente. Creare una copia del uisample.msi e spostarla nella stessa directory contenente la cartella Blocco note creata in [Pianificazione dell'installazione](planning-the-installation.md)di . Rinominare il file MNP2000.msi. Il file del database di installazione e i file di origine devono trovarsi entrambi nella radice della stessa directory. Esempio:

C: \\ Esempi \\MNP2000.msi

C: \\ Esempi \\ Blocco note\\

Se non si usa Uisample.msi, è necessario ottenere un database vuoto, ad esempio Schema.msi, e immettere le informazioni per l'installazione usando uno strumento di modifica del database come Orca, fornito con l'SDK, o un altro editor di database.

[Continua](specifying-directory-structure.md)

 

 



