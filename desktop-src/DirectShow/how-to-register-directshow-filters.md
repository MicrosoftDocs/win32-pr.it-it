---
description: Come registrare i filtri DirectShow
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Come registrare i filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401185"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="97341-103">Come registrare i filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="97341-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="97341-104">Questo articolo descrive come creare un filtro Microsoft DirectShow con registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="97341-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="97341-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97341-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="97341-106">Layout delle chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="97341-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="97341-107">Dichiarazione delle informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="97341-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="97341-108">Dichiarazione del modello Factory</span><span class="sxs-lookup"><span data-stu-id="97341-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="97341-109">Implementazione di DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="97341-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="97341-110">Linee guida per la registrazione dei filtri</span><span class="sxs-lookup"><span data-stu-id="97341-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="97341-111">Annullamento della registrazione di un filtro</span><span class="sxs-lookup"><span data-stu-id="97341-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="97341-112">Questo articolo non descrive come creare una DLL per un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="97341-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="97341-113">Per informazioni sulla creazione di dll, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="97341-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="97341-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97341-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97341-115">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="97341-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



