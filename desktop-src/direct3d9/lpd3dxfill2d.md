---
description: Tipo di funzione usato dalle funzioni di riempimento della trama.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225352"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="13f98-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="13f98-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="13f98-104">Tipo di funzione usato dalle funzioni di riempimento della trama.</span><span class="sxs-lookup"><span data-stu-id="13f98-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13f98-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="13f98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13f98-106">Parameters</span></span>

<span data-ttu-id="13f98-107">Puntatore broncio a un vettore, usato dalla funzione per restituirne il risultato.</span><span class="sxs-lookup"><span data-stu-id="13f98-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="13f98-108">Verrà eseguito il mapping di X, Y, Z e W rispettivamente a R, G, B e A.</span><span class="sxs-lookup"><span data-stu-id="13f98-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="13f98-109">pTexCoord: puntatore a un vettore che contiene le coordinate del Texel attualmente in fase di valutazione.</span><span class="sxs-lookup"><span data-stu-id="13f98-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="13f98-110">I componenti delle coordinate di trama per trama e trama del volume variano da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="13f98-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="13f98-111">I componenti delle coordinate di trama per le trame del cubo variano da-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="13f98-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="13f98-112">pTexelSize: puntatore a un vettore che contiene le dimensioni del Texel corrente.</span><span class="sxs-lookup"><span data-stu-id="13f98-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="13f98-113">pData: puntatore ai dati utente.</span><span class="sxs-lookup"><span data-stu-id="13f98-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="13f98-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13f98-114">Return Value</span></span>

<span data-ttu-id="13f98-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="13f98-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f98-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="13f98-116">Remarks</span></span>

<span data-ttu-id="13f98-117">Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="13f98-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="13f98-118">In caso contrario, è possibile che si verifichino overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="13f98-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="13f98-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13f98-119">Header</span></span>                   | <span data-ttu-id="13f98-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="13f98-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="13f98-121">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="13f98-121">Import Library</span></span>           | <span data-ttu-id="13f98-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="13f98-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="13f98-123">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="13f98-123">Minimum Operating System</span></span> | <span data-ttu-id="13f98-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="13f98-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="13f98-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13f98-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f98-126">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="13f98-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="13f98-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="13f98-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
