---
title: Registro di nebbia
description: Questo registro di output del vertex shader contiene un colore per la nebbia per vertice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976103"
---
# <a name="fog-register"></a><span data-ttu-id="64aca-103">Registro di nebbia</span><span class="sxs-lookup"><span data-stu-id="64aca-103">Fog Register</span></span>

<span data-ttu-id="64aca-104">Questo registro di output del vertex shader contiene un colore per la nebbia per vertice.</span><span class="sxs-lookup"><span data-stu-id="64aca-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="64aca-105">Un registro è costituito da proprietà che determinano il comportamento di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="64aca-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="64aca-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64aca-106">Property</span></span>        | <span data-ttu-id="64aca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64aca-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64aca-108">Nome</span><span class="sxs-lookup"><span data-stu-id="64aca-108">Name</span></span>            | <span data-ttu-id="64aca-109">oFog</span><span class="sxs-lookup"><span data-stu-id="64aca-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="64aca-110">Conteggio</span><span class="sxs-lookup"><span data-stu-id="64aca-110">Count</span></span>           | <span data-ttu-id="64aca-111">Un vettore, di cui è possibile usare un solo componente e che deve essere specificato dalla maschera dei componenti</span><span class="sxs-lookup"><span data-stu-id="64aca-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="64aca-112">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="64aca-112">I/O permissions</span></span> | <span data-ttu-id="64aca-113">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="64aca-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="64aca-114">Il valore di nebbia di output viene registrato.</span><span class="sxs-lookup"><span data-stu-id="64aca-114">The output fog value registers.</span></span> <span data-ttu-id="64aca-115">Il valore è il fattore di nebbia da interpolare e quindi indirizzato alla tabella Fog.</span><span class="sxs-lookup"><span data-stu-id="64aca-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="64aca-116">Viene utilizzato solo il componente x scalare della nebbia.</span><span class="sxs-lookup"><span data-stu-id="64aca-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64aca-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64aca-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64aca-118">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="64aca-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




