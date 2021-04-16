---
description: Per le trasformazioni con percorso completo è necessario che un'origine si trovi nel percorso completo specificato nella proprietà Transforms.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Trasformazioni protette con percorso completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530301"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="0804e-103">Trasformazioni protette con percorso completo</span><span class="sxs-lookup"><span data-stu-id="0804e-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="0804e-104">Per le trasformazioni con percorso completo è necessario che un'origine si trovi nel percorso completo specificato nella proprietà [**TRANSforms**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="0804e-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="0804e-105">Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="0804e-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="0804e-106">Se la copia locale della trasformazione non è più disponibile, può ripristinare solo la cache usando il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="0804e-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="0804e-107">La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per il prodotto dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0804e-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="0804e-108">Per applicare le trasformazioni Secure-Full-Paths durante l'installazione di un pacchetto, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o rendere \| il primo carattere passato nell'elenco di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="0804e-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="0804e-109">I percorsi completi dell'origine di ogni trasformazione devono essere passati nella stringa Transforms.</span><span class="sxs-lookup"><span data-stu-id="0804e-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="0804e-110">Se nell'elenco sono presenti percorsi relativi, l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="0804e-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="0804e-111">Non è necessario che l'origine della trasformazione si trovi con l'origine del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0804e-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



