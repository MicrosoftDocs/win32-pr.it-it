---
description: 'LPD3DXFILL2D: tipo di funzione usato dalle funzioni di riempimento della trama.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c341ccfcbcc566d65e7139813c676e2286e25cf
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342846"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="c5958-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="c5958-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="c5958-104">Tipo di funzione usato dalle funzioni di riempimento della trama.</span><span class="sxs-lookup"><span data-stu-id="c5958-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5958-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5958-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="c5958-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5958-106">Parameters</span></span>

<span data-ttu-id="c5958-107">pOut: puntatore a un vettore, che la funzione usa per restituire il risultato.</span><span class="sxs-lookup"><span data-stu-id="c5958-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="c5958-108">X, Y, Z e W verranno mappati rispettivamente a R, G, B e A.</span><span class="sxs-lookup"><span data-stu-id="c5958-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="c5958-109">pTexCoord: puntatore a un vettore contenente le coordinate del texel attualmente valutato.</span><span class="sxs-lookup"><span data-stu-id="c5958-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="c5958-110">I componenti delle coordinate di trama per le trame di trama e volume sono da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="c5958-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="c5958-111">I componenti delle coordinate di trama per le trame del cubo variano da -1 a 1.</span><span class="sxs-lookup"><span data-stu-id="c5958-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="c5958-112">pTexelSize: puntatore a un vettore contenente le dimensioni del texel corrente.</span><span class="sxs-lookup"><span data-stu-id="c5958-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="c5958-113">pData: puntatore ai dati utente.</span><span class="sxs-lookup"><span data-stu-id="c5958-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5958-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5958-114">Return Value</span></span>

<span data-ttu-id="c5958-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c5958-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5958-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5958-116">Remarks</span></span>

<span data-ttu-id="c5958-117">Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c5958-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="c5958-118">In caso contrario, possono verificarsi overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="c5958-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="c5958-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5958-119">Requirement</span></span>                         | <span data-ttu-id="c5958-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5958-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c5958-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5958-121">Header</span></span>                   | <span data-ttu-id="c5958-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="c5958-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="c5958-123">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="c5958-123">Import Library</span></span>           | <span data-ttu-id="c5958-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="c5958-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="c5958-125">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="c5958-125">Minimum Operating System</span></span> | <span data-ttu-id="c5958-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c5958-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c5958-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5958-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5958-128">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="c5958-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="c5958-129">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="c5958-129">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
