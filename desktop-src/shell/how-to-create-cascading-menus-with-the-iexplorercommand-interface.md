---
description: "Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare IExplorerCommand:: EnumSubCommands."
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Creare menu a cascata con l'interfaccia IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550997"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="b4ab1-103">Come creare menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="b4ab1-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="b4ab1-104">Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="b4ab1-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="b4ab1-105">Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando tramite l'interfaccia [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di utilizzare tali comandi come verbi in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b4ab1-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="b4ab1-106">In Windows 7 e versioni successive, è possibile fornire la stessa implementazione del verbo usando l'interfaccia [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , come è possibile con l'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="b4ab1-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="b4ab1-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="b4ab1-107">Instructions</span></span>


<span data-ttu-id="b4ab1-108">Le due schermate seguenti illustrano l'uso dei menu a cascata nella cartella **Devices** .</span><span class="sxs-lookup"><span data-stu-id="b4ab1-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot che mostra un esempio di menu a cascata nella cartella Devices (dispositivi).](images/file-assoc/filecascademenu.png)

![screenshot che mostra un esempio di menu a cascata nella cartella Devices](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="b4ab1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4ab1-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4ab1-112">Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usare le origini dati della shell che devono condividere l'implementazione tra i comandi e i menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b4ab1-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b4ab1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4ab1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4ab1-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="b4ab1-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="b4ab1-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="b4ab1-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="b4ab1-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="b4ab1-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
