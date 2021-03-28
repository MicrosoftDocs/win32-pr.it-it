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
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="9d798-103">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="9d798-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="9d798-104">In Windows 7 e versioni successive, l'implementazione del menu a cascata è supportata tramite le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9d798-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="9d798-105">Prima di Windows 7, la creazione dei menu a cascata era possibile solo tramite l'implementazione dell'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="9d798-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="9d798-106">In Windows 7 e versioni successive, è consigliabile ricorrere a soluzioni basate su codice Component Object Model (COM) solo quando i metodi statici sono insufficienti.</span><span class="sxs-lookup"><span data-stu-id="9d798-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="9d798-107">Lo screenshot seguente fornisce un esempio di menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="9d798-107">The following screen shot provides an example of a cascading menu.</span></span>

![screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="9d798-109">In Windows 7 e versioni successive sono disponibili tre modi per creare i menu a cascata, descritti nelle sezioni riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9d798-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="9d798-110">Come creare menu a cascata con la voce del registro di sistema sottocomandi</span><span class="sxs-lookup"><span data-stu-id="9d798-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="9d798-111">Come creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="9d798-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="9d798-112">Come creare menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="9d798-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
