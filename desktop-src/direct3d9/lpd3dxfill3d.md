---
description: Tipo di funzione usato dalle funzioni di riempimento della trama.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97342895cb119a786aa71626aeea6d93650c6dc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482053"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="9f865-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="9f865-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="9f865-104">Tipo di funzione usato dalle funzioni di riempimento della trama.</span><span class="sxs-lookup"><span data-stu-id="9f865-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f865-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f865-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="9f865-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f865-106">Parameters</span></span>

<span data-ttu-id="9f865-107">Puntatore broncio a un vettore, usato dalla funzione per restituirne il risultato.</span><span class="sxs-lookup"><span data-stu-id="9f865-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="9f865-108">Verrà eseguito il mapping di X, Y, Z e W rispettivamente a R, G, B e A.</span><span class="sxs-lookup"><span data-stu-id="9f865-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="9f865-109">pTexCoord: puntatore a un vettore che contiene le coordinate del Texel attualmente in fase di valutazione.</span><span class="sxs-lookup"><span data-stu-id="9f865-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="9f865-110">I componenti delle coordinate di trama per trama e trama del volume variano da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="9f865-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="9f865-111">I componenti delle coordinate di trama per le trame del cubo variano da-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="9f865-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="9f865-112">pTexelSize: puntatore a un vettore che contiene le dimensioni del Texel corrente.</span><span class="sxs-lookup"><span data-stu-id="9f865-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="9f865-113">pData: puntatore ai dati utente.</span><span class="sxs-lookup"><span data-stu-id="9f865-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f865-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f865-114">Return Value</span></span>

<span data-ttu-id="9f865-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9f865-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f865-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f865-116">Remarks</span></span>

<span data-ttu-id="9f865-117">Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="9f865-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="9f865-118">In caso contrario, è possibile che si verifichino overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="9f865-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9f865-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f865-119">Header</span></span>                   | <span data-ttu-id="9f865-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="9f865-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="9f865-121">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="9f865-121">Import Library</span></span>           | <span data-ttu-id="9f865-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="9f865-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="9f865-123">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="9f865-123">Minimum Operating System</span></span> | <span data-ttu-id="9f865-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9f865-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9f865-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f865-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f865-126">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="9f865-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="9f865-127">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="9f865-127">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
