---
description: Per aggiungere un elemento al sottomenu programmi, attenersi alla seguente procedura.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Come aggiungere collegamenti al menu Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131630"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="c6b91-103">Come aggiungere collegamenti al menu Start</span><span class="sxs-lookup"><span data-stu-id="c6b91-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="c6b91-104">Per aggiungere un elemento al sottomenu **programmi** , attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="c6b91-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="c6b91-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c6b91-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c6b91-106">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="c6b91-106">Step 1:</span></span>

<span data-ttu-id="c6b91-107">Creare un [collegamento della shell](./links.md) usando l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="c6b91-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="c6b91-108">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="c6b91-108">Step 2:</span></span>

<span data-ttu-id="c6b91-109">Ottenere il percorso della cartella programmi usando la funzione [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , passando i [**\_ programmi FOLDERID**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="c6b91-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="c6b91-110">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="c6b91-110">Step 3:</span></span>

<span data-ttu-id="c6b91-111">Aggiungere il collegamento della shell alla cartella programmi.</span><span class="sxs-lookup"><span data-stu-id="c6b91-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="c6b91-112">È anche possibile creare una cartella nella cartella programmi e aggiungere il collegamento a tale cartella.</span><span class="sxs-lookup"><span data-stu-id="c6b91-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
