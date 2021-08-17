---
description: A Windows 7, i menu a cascata vengono creati tramite la voce del Registro di sistema SubCommands, la voce del Registro di sistema ExtendedSubCommandsKey o l'interfaccia IExplorerCommand.
title: Creazione di menu a cascata statici
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456331"
---
# <a name="creating-static-cascading-menus"></a>Creazione di menu a cascata statici

In Windows 7 e versioni successive l'implementazione del menu a cascata è supportata tramite le impostazioni del Registro di sistema. Nelle versioni Windows 7, la creazione di menu a cascata era possibile solo tramite l'implementazione [**dell'interfaccia IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) In Windows 7 e versioni successive è consigliabile ricorrere a soluzioni basate su codice Component Object Model (COM) solo quando i metodi statici non sono sufficienti.

Lo screenshot seguente fornisce un esempio di menu a cascata.

![Screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 e versioni successive sono disponibili tre modi per creare menu a cascata, descritti nelle sezioni seguenti.

-   [Come creare menu a cascata con la voce del Registro di sistema SubCommands](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Come creare menu a cascata con la voce del Registro di sistema ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Come creare menu a cascata con l'interfaccia IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
