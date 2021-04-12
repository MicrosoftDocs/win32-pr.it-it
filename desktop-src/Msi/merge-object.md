---
description: L'oggetto merge consente di accedere ad altri oggetti di primo livello. Prima di caricare il supporto di automazione richiesto da COM per accedere alle funzioni in Mergemod.dll, è necessario creare un oggetto merge.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Merge (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233847"
---
# <a name="merge-object"></a><span data-ttu-id="9d959-104">Merge (oggetto)</span><span class="sxs-lookup"><span data-stu-id="9d959-104">Merge Object</span></span>

<span data-ttu-id="9d959-105">L'oggetto **merge** consente di accedere ad altri oggetti di primo livello.</span><span class="sxs-lookup"><span data-stu-id="9d959-105">The **Merge** object provides access to other top-level objects.</span></span> <span data-ttu-id="9d959-106">Prima di caricare il supporto di automazione richiesto da COM per accedere alle funzioni in Mergemod.dll, è necessario creare un oggetto **merge** .</span><span class="sxs-lookup"><span data-stu-id="9d959-106">A **Merge** object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.</span></span>

<span data-ttu-id="9d959-107">Mergemod.dll fornisce accesso alle funzionalità estese in fase di compilazione tramite una seconda versione del CLSID esistente.</span><span class="sxs-lookup"><span data-stu-id="9d959-107">Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID.</span></span> <span data-ttu-id="9d959-108">Questo CLSID supporta la funzionalità esistente disponibile tramite l'interfaccia [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , ma l'interfaccia predefinita nell'oggetto (e l'interfaccia duale associata) è l'interfaccia [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) anziché l'interfaccia **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="9d959-108">This CLSID supports existing functionality available through the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) interface, but the default interface on the object (and the associated dual interface) is the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface instead of the **IMsmMerge** interface.</span></span>

 

 
