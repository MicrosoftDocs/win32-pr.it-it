---
title: Funzioni di trasformazione vettoriale 3D DirectXMath
description: Elenca le funzioni di trasformazione vettoriale 3D.
ms.assetid: 148972da-e460-63b9-6b01-10201f63d157
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a592071970d69d7ef4b4db42960335c5fc771ac3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309271"
---
# <a name="directxmath-3d-vector-transformation-functions"></a><span data-ttu-id="2ca56-103">Funzioni di trasformazione vettoriale 3D DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2ca56-103">DirectXMath 3D vector transformation functions</span></span>

<span data-ttu-id="2ca56-104">Elenca le funzioni di trasformazione vettoriale 3D.</span><span class="sxs-lookup"><span data-stu-id="2ca56-104">Lists the 3D vector transformation functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ca56-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2ca56-105">In this section</span></span>



| <span data-ttu-id="2ca56-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="2ca56-106">Topic</span></span>                                                                               | <span data-ttu-id="2ca56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ca56-107">Description</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ca56-108">**XMVector3InverseRotate**</span><span class="sxs-lookup"><span data-stu-id="2ca56-108">**XMVector3InverseRotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3inverserotate)<br/>                 | <span data-ttu-id="2ca56-109">Ruota un vettore 3D usando l'inverso di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="2ca56-109">Rotates a 3D vector using the inverse of a quaternion.</span></span><br/>                                                                                |
| [<span data-ttu-id="2ca56-110">**XMVector3Project**</span><span class="sxs-lookup"><span data-stu-id="2ca56-110">**XMVector3Project**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)<br/>                             | <span data-ttu-id="2ca56-111">Proiettare un vettore 3D dallo spazio oggetto nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2ca56-111">Project a 3D vector from object space into screen space.</span></span><br/>                                                                              |
| [<span data-ttu-id="2ca56-112">**XMVector3ProjectStream**</span><span class="sxs-lookup"><span data-stu-id="2ca56-112">**XMVector3ProjectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)<br/>                 | <span data-ttu-id="2ca56-113">Proietta un flusso di vettori 3D dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2ca56-113">Projects a stream of 3D vectors from object space into screen space.</span></span><br/>                                                                  |
| [<span data-ttu-id="2ca56-114">**XMVector3Rotate**</span><span class="sxs-lookup"><span data-stu-id="2ca56-114">**XMVector3Rotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3rotate)<br/>                               | <span data-ttu-id="2ca56-115">Ruota un vettore 3D usando un quaternione.</span><span class="sxs-lookup"><span data-stu-id="2ca56-115">Rotates a 3D vector using a quaternion.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2ca56-116">**XMVector3Transform**</span><span class="sxs-lookup"><span data-stu-id="2ca56-116">**XMVector3Transform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)<br/>                         | <span data-ttu-id="2ca56-117">Trasforma un vettore 3D in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="2ca56-117">Transforms a 3D vector by a matrix.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2ca56-118">**XMVector3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="2ca56-118">**XMVector3TransformCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)<br/>               | <span data-ttu-id="2ca56-119">Trasforma un vettore 3D in base a una matrice specificata, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="2ca56-119">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span><br/>                                                      |
| [<span data-ttu-id="2ca56-120">**XMVector3TransformCoordStream**</span><span class="sxs-lookup"><span data-stu-id="2ca56-120">**XMVector3TransformCoordStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)<br/>   | <span data-ttu-id="2ca56-121">Trasforma un flusso di vettori 3D da una matrice specificata, proiettando i vettori risultanti in modo che le rispettive coordinate w siano uguali a 1,0.</span><span class="sxs-lookup"><span data-stu-id="2ca56-121">Transforms a stream of 3D vectors by a given matrix, projecting the resulting vectors such that their w coordinates are equal to 1.0.</span></span><br/> |
| [<span data-ttu-id="2ca56-122">**XMVector3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="2ca56-122">**XMVector3TransformNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)<br/>             | <span data-ttu-id="2ca56-123">Trasforma il vettore 3D normale dalla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="2ca56-123">Transforms the 3D vector normal by the given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="2ca56-124">**XMVector3TransformNormalStream**</span><span class="sxs-lookup"><span data-stu-id="2ca56-124">**XMVector3TransformNormalStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)<br/> | <span data-ttu-id="2ca56-125">Trasforma un flusso di vettori normali 3D da una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="2ca56-125">Transforms a stream of 3D normal vectors by a given matrix.</span></span><br/>                                                                           |
| [<span data-ttu-id="2ca56-126">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="2ca56-126">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)<br/>             | <span data-ttu-id="2ca56-127">Trasforma un flusso di vettori 3D in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="2ca56-127">Transforms a stream of 3D vectors by a given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="2ca56-128">**XMVector3Unproject**</span><span class="sxs-lookup"><span data-stu-id="2ca56-128">**XMVector3Unproject**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)<br/>                         | <span data-ttu-id="2ca56-129">Proietta un vettore 3D dallo spazio dello schermo nello spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="2ca56-129">Projects a 3D vector from screen space into object space.</span></span><br/>                                                                             |
| [<span data-ttu-id="2ca56-130">**XMVector3UnprojectStream**</span><span class="sxs-lookup"><span data-stu-id="2ca56-130">**XMVector3UnprojectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)<br/>             | <span data-ttu-id="2ca56-131">Trasforma un flusso di vettori 3D dallo spazio dello schermo allo spazio degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="2ca56-131">Transforms a stream of 3D vectors from screen space to object space.</span></span><br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="2ca56-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ca56-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca56-133">Funzioni Vector 3D della libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2ca56-133">DirectXMath Library 3D Vector Functions</span></span>](ovw-xnamath-reference-functions-vector3.md)
</dt> </dl>

 

 
