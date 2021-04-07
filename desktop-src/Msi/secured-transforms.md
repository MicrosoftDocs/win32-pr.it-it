---
description: Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Trasformazioni protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885685"
---
# <a name="secured-transforms"></a><span data-ttu-id="cefc1-103">Trasformazioni protette</span><span class="sxs-lookup"><span data-stu-id="cefc1-103">Secured Transforms</span></span>

<span data-ttu-id="cefc1-104">Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cefc1-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="cefc1-105">Le trasformazioni protette vengono archiviate localmente nel computer dell'utente in una posizione in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="cefc1-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="cefc1-106">Tali trasformazioni vengono memorizzate nella cache in questa posizione durante l'installazione o l'annuncio del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cefc1-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="cefc1-107">Solo gli amministratori e il sistema locale hanno accesso in scrittura a questo percorso.</span><span class="sxs-lookup"><span data-stu-id="cefc1-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="cefc1-108">Un utente non amministratore non sarà in grado di modificare il file di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="cefc1-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="cefc1-109">Durante le installazioni successive di [installazione su richiesta](installation-on-demand.md) o [manutenzione](maintenance-installation.md) del pacchetto, il programma di installazione usa le trasformazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="cefc1-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="cefc1-110">Per specificare l'archiviazione di trasformazione protetta, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md), impostare la proprietà [**TRANSFORMSSECURE**](transformssecure.md) oppure passare il simbolo @ o \| nell'elenco trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="cefc1-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="cefc1-111">Si noti che non è possibile includere trasformazioni protette e non protette nello stesso elenco di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="cefc1-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="cefc1-112">Vedere [applicazione di trasformazioni](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="cefc1-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="cefc1-113">La rimozione del prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni protette per il prodotto dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cefc1-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="cefc1-114">Se il programma di installazione rileva che una trasformazione protetta non è disponibile localmente, tenta di ripristinare la cache di trasformazione da un'origine.</span><span class="sxs-lookup"><span data-stu-id="cefc1-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="cefc1-115">Le trasformazioni protette possono essere sicure all'origine o protette-Full-Path:</span><span class="sxs-lookup"><span data-stu-id="cefc1-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="cefc1-116">Le [trasformazioni protette a livello di origine](secure-at-source-transforms.md) mancanti dalla cache di trasformazione locale vengono ripristinate dalla radice dell'origine del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="cefc1-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="cefc1-117">Le [trasformazioni protette con percorso completo](secure-full-path-transforms.md) mancanti dalla cache di trasformazione locale vengono ripristinate dal percorso completo originale specificato dall'elenco Transforms.</span><span class="sxs-lookup"><span data-stu-id="cefc1-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



