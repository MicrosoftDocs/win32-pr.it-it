---
description: A partire da Windows 7, i menu a cascata vengono creati tramite la voce del registro di sistema subcommands, la voce del registro di sistema ExtendedSubCommandsKey o l'interfaccia IExplorerCommand.
title: Creazione di menu a cascata statici
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555986"
---
# <a name="creating-static-cascading-menus"></a>Creazione di menu a cascata statici

In Windows 7 e versioni successive, l'implementazione del menu a cascata è supportata tramite le impostazioni del registro di sistema. Prima di Windows 7, la creazione dei menu a cascata era possibile solo tramite l'implementazione dell'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . In Windows 7 e versioni successive, è consigliabile ricorrere a soluzioni basate su codice Component Object Model (COM) solo quando i metodi statici sono insufficienti.

Lo screenshot seguente fornisce un esempio di menu a cascata.

![screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 e versioni successive sono disponibili tre modi per creare i menu a cascata, descritti nelle sezioni riportate di seguito.

-   [Come creare menu a cascata con la voce del registro di sistema sottocomandi](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Come creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Come creare menu a cascata con l'interfaccia IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
