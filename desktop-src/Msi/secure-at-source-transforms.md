---
description: Le trasformazioni sicure all'origine devono disporre di un'origine che si trova nella radice dell'origine per il pacchetto.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Trasformazioni protette a livello di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885686"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="65555-103">Trasformazioni protette a livello di origine</span><span class="sxs-lookup"><span data-stu-id="65555-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="65555-104">Le trasformazioni sicure all'origine devono disporre di un'origine che si trova nella radice dell'origine per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="65555-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="65555-105">Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="65555-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="65555-106">Se la copia locale della trasformazione diventa non disponibile, il programma di installazione cerca un'origine per ripristinare la cache.</span><span class="sxs-lookup"><span data-stu-id="65555-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="65555-107">Il metodo è identico a quello di ricerca nell'elenco di origine di un file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="65555-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="65555-108">Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="65555-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="65555-109">La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per il prodotto dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="65555-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="65555-110">Per applicare le trasformazioni sicure all'origine durante l'installazione di un pacchetto, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) oppure fare in modo che @ il primo carattere passato nell'elenco di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="65555-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="65555-111">Ogni trasformazione deve essere indicata da un nome di file e deve trovarsi nella radice dell'origine del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="65555-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="65555-112">Se una delle trasformazioni non si trova nella radice dell'origine del pacchetto, l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="65555-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="65555-113">Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="65555-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



