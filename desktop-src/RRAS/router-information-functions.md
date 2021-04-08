---
title: Funzioni per informazioni sul router
description: Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni sul router. Un'intestazione informazioni è costituita da blocchi di informazioni e metadati privati. I blocchi di informazioni sono matrici di strutture di informazioni di diversi tipi.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043983"
---
# <a name="router-information-functions"></a><span data-ttu-id="b24da-105">Funzioni per informazioni sul router</span><span class="sxs-lookup"><span data-stu-id="b24da-105">Router Information Functions</span></span>

<span data-ttu-id="b24da-106">Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni sul router.</span><span class="sxs-lookup"><span data-stu-id="b24da-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="b24da-107">Un'intestazione informazioni è costituita da blocchi di informazioni e metadati privati.</span><span class="sxs-lookup"><span data-stu-id="b24da-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="b24da-108">I blocchi di informazioni sono matrici di [strutture di informazioni](router-information-structures.md) di diversi [tipi](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="b24da-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="b24da-109">Le funzioni seguenti modificano le intestazioni delle informazioni:</span><span class="sxs-lookup"><span data-stu-id="b24da-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="b24da-110">**MprInfoCreate**</span><span class="sxs-lookup"><span data-stu-id="b24da-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="b24da-111">**MprInfoDelete**</span><span class="sxs-lookup"><span data-stu-id="b24da-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="b24da-112">**MprInfoDuplicate**</span><span class="sxs-lookup"><span data-stu-id="b24da-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="b24da-113">**MprInfoRemoveAll**</span><span class="sxs-lookup"><span data-stu-id="b24da-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="b24da-114">Le funzioni seguenti modificano i blocchi di informazioni all'interno di un'intestazione di informazioni:</span><span class="sxs-lookup"><span data-stu-id="b24da-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="b24da-115">**MprInfoBlockAdd**</span><span class="sxs-lookup"><span data-stu-id="b24da-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="b24da-116">**MprInfoBlockFind**</span><span class="sxs-lookup"><span data-stu-id="b24da-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="b24da-117">**MprInfoBlockQuerySize**</span><span class="sxs-lookup"><span data-stu-id="b24da-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="b24da-118">**MprInfoBlockRemove**</span><span class="sxs-lookup"><span data-stu-id="b24da-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="b24da-119">**MprInfoBlockSet**</span><span class="sxs-lookup"><span data-stu-id="b24da-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="b24da-120">Molte delle [funzioni di amministrazione e configurazione del router](understanding-mprinfo-functions-and-information-headers.md) utilizzano le intestazioni delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="b24da-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




