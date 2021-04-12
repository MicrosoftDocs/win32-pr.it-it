---
description: Quando si installa una patch e una o più trasformazioni di personalizzazione in un'applicazione, la patch viene in genere installata per prima, seguita dalle trasformazioni di personalizzazione.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Applicazione di patch a applicazioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345551"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="9619c-103">Applicazione di patch a applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="9619c-103">Patching Customized Applications</span></span>

<span data-ttu-id="9619c-104">Quando si installa una patch e una o più trasformazioni di personalizzazione in un'applicazione, la patch viene in genere installata per prima, seguita dalle trasformazioni di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="9619c-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="9619c-105">Per impostazione predefinita, la patch non è interruppe dalla successiva installazione della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="9619c-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="9619c-106">Tuttavia, l'installazione iniziale delle trasformazioni e quindi della patch potrebbe interrompere la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="9619c-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="9619c-107">È ad esempio possibile che si verifichi un'interruzioni della personalizzazione quando si usa una patch per aggiornare un prodotto dalla versione 1 alla versione 2 e una trasformazione di personalizzazione che funziona per la versione 1 non funziona per la versione 2.</span><span class="sxs-lookup"><span data-stu-id="9619c-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="9619c-108">In questo caso, la patch di aggiornamento della versione non può essere applicata a un prodotto personalizzato senza prima disinstallare e reinstallare il prodotto originale.</span><span class="sxs-lookup"><span data-stu-id="9619c-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



