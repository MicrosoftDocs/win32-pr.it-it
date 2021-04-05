---
description: Uso dei menu creati dal proprietario per supportare la funzionalità di riconoscimento vocale per il Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Uso di menu Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751271"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="a3421-103">Uso di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a3421-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="a3421-104">Quando si usano i menu creati dal proprietario, è necessario rendere disponibili i nomi di menu per supportare la funzionalità di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="a3421-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="a3421-105">A questo scopo è possibile procedere in due modi:</span><span class="sxs-lookup"><span data-stu-id="a3421-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="a3421-106">Esporre il nome della voce di menu utilizzando la struttura MSAAMENUINFO.</span><span class="sxs-lookup"><span data-stu-id="a3421-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="a3421-107">Consente di sostituire i menu grafici con i menu di testo standard quando è attivo un supporto per l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="a3421-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="a3421-108">Se la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) restituisce **true** con il relativo parametro *uiAction* impostato su SPI \_ GETSCREENREADER, usare i menu standard. L'applicazione deve controllare il messaggio WM \_ SETTINGSCHANGE e rispondere eseguendo una query sullo stato di questa opzione e modificando in modo appropriato la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a3421-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="a3421-109">Microsoft Visual Studio, ad esempio, offre un'opzione per utilizzare i menu standard anziché i menu personalizzati visualizzati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a3421-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
