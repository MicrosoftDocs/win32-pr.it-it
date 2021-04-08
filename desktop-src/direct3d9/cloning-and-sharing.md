---
description: Clonazione e condivisione (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonazione e condivisione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878274"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="14c3c-103">Clonazione e condivisione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="14c3c-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="14c3c-104">Parametri di clonazione</span><span class="sxs-lookup"><span data-stu-id="14c3c-104">Cloning Parameters</span></span>

<span data-ttu-id="14c3c-105">La clonazione presenta le restrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="14c3c-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="14c3c-106">I cloni ereditano il pool dell'effetto originale.</span><span class="sxs-lookup"><span data-stu-id="14c3c-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="14c3c-107">Vedere la sezione relativa ai parametri di condivisione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="14c3c-108">I cloni ereditano le tecniche, le sessioni, i parametri e le annotazioni dell'effetto originale (incluse tutte le annotazioni aggiunte con [**ID3DXEffect**](id3dxeffect.md)).</span><span class="sxs-lookup"><span data-stu-id="14c3c-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="14c3c-109">I cloni ereditano le annotazioni aggiunte dinamicamente dall'effetto originale.</span><span class="sxs-lookup"><span data-stu-id="14c3c-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="14c3c-110">La clonazione su un nuovo dispositivo non riuscirà se il pool dell'effetto originale non era **null** e l'effetto originale conteneva un parametro condiviso dipendente dal dispositivo, ad esempio una trama o uno shader.</span><span class="sxs-lookup"><span data-stu-id="14c3c-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="14c3c-111">Condivisione di parametri</span><span class="sxs-lookup"><span data-stu-id="14c3c-111">Sharing Parameters</span></span>

<span data-ttu-id="14c3c-112">Un pool è un buffer che condivide parametri di effetto tra diversi effetti.</span><span class="sxs-lookup"><span data-stu-id="14c3c-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="14c3c-113">Per aggiungere parametri a un pool, specificare un utilizzo condiviso quando viene creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="14c3c-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="14c3c-114">Un pool presenta le restrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="14c3c-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="14c3c-115">Un parametro viene aggiunto al pool la prima volta che un effetto contenente il parametro (condiviso) viene aggiunto al pool.</span><span class="sxs-lookup"><span data-stu-id="14c3c-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="14c3c-116">Un pool ottiene i valori iniziali dal primo parametro condiviso. i parametri condivisi successivamente ottengono i valori dal pool.</span><span class="sxs-lookup"><span data-stu-id="14c3c-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="14c3c-117">Un parametro viene eliminato dal pool quando vengono rilasciati tutti i riferimenti di effetto al parametro condiviso.</span><span class="sxs-lookup"><span data-stu-id="14c3c-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="14c3c-118">Tutti gli effetti nel pool che contengono lo stesso parametro (Shared) dipendente dal dispositivo devono avere lo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14c3c-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="14c3c-119">È possibile utilizzare **null** per specificare nessun pool, nel qual caso non viene condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="14c3c-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="14c3c-120">Questa operazione è quasi equivalente alla specifica di un pool univoco solo per questo effetto.</span><span class="sxs-lookup"><span data-stu-id="14c3c-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="14c3c-121">L'unica differenza è che quando l'effetto viene clonato, il clone non condividerà i parametri condivisi con quello originale.</span><span class="sxs-lookup"><span data-stu-id="14c3c-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14c3c-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14c3c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14c3c-123">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="14c3c-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



