---
title: Registro dimensioni punti
description: Questo registro di output del vertex shader contiene dati di dimensione del punto per vertice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395803"
---
# <a name="point-size-register"></a><span data-ttu-id="02e32-103">Registro dimensioni punti</span><span class="sxs-lookup"><span data-stu-id="02e32-103">Point Size Register</span></span>

<span data-ttu-id="02e32-104">Questo registro di output del vertex shader contiene dati di dimensione del punto per vertice.</span><span class="sxs-lookup"><span data-stu-id="02e32-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="02e32-105">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="02e32-105">Vertex shader versions</span></span> | <span data-ttu-id="02e32-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="02e32-106">1\_1</span></span> | <span data-ttu-id="02e32-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02e32-107">2\_0</span></span> | <span data-ttu-id="02e32-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="02e32-108">2\_sw</span></span> | <span data-ttu-id="02e32-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="02e32-109">2\_x</span></span> | <span data-ttu-id="02e32-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02e32-110">3\_0</span></span> | <span data-ttu-id="02e32-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="02e32-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="02e32-112">Registro dimensioni punti</span><span class="sxs-lookup"><span data-stu-id="02e32-112">Point Size Register</span></span>    | <span data-ttu-id="02e32-113">x</span><span class="sxs-lookup"><span data-stu-id="02e32-113">x</span></span>    | <span data-ttu-id="02e32-114">x</span><span class="sxs-lookup"><span data-stu-id="02e32-114">x</span></span>    | <span data-ttu-id="02e32-115">x</span><span class="sxs-lookup"><span data-stu-id="02e32-115">x</span></span>     | <span data-ttu-id="02e32-116">x</span><span class="sxs-lookup"><span data-stu-id="02e32-116">x</span></span>    | <span data-ttu-id="02e32-117">x</span><span class="sxs-lookup"><span data-stu-id="02e32-117">x</span></span>    | <span data-ttu-id="02e32-118">x</span><span class="sxs-lookup"><span data-stu-id="02e32-118">x</span></span>     |



 

<span data-ttu-id="02e32-119">Un registro è costituito da proprietà che determinano il comportamento di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="02e32-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="02e32-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e32-120">Property</span></span>        | <span data-ttu-id="02e32-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02e32-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e32-122">Nome</span><span class="sxs-lookup"><span data-stu-id="02e32-122">Name</span></span>            | <span data-ttu-id="02e32-123">oPts</span><span class="sxs-lookup"><span data-stu-id="02e32-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="02e32-124">Conteggio</span><span class="sxs-lookup"><span data-stu-id="02e32-124">Count</span></span>           | <span data-ttu-id="02e32-125">1 vettore, di cui è possibile utilizzare solo un componente e che deve essere specificato dalla maschera dei componenti.</span><span class="sxs-lookup"><span data-stu-id="02e32-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="02e32-126">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="02e32-126">I/O permissions</span></span> | <span data-ttu-id="02e32-127">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="02e32-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="02e32-128">Viene utilizzato solo il componente x scalare della dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="02e32-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02e32-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02e32-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e32-130">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="02e32-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




