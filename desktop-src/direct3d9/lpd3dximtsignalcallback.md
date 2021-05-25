---
description: Prototipo di funzione usato da D3DXComputeIMTFromSignal per descrivere un segnale definito dall'utente nello spazio u,v di una mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension in corrispondenza della coordinata u,v specificata.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342836"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="26c3a-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="26c3a-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="26c3a-105">Prototipo di funzione [**usato da D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) per descrivere un segnale definito dall'utente nello spazio u,v di una mesh di input.</span><span class="sxs-lookup"><span data-stu-id="26c3a-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="26c3a-106">La funzione valuta un segnale procedurale della dimensione uSignalDimension in corrispondenza della coordinata u,v specificata.</span><span class="sxs-lookup"><span data-stu-id="26c3a-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c3a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26c3a-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="26c3a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="26c3a-108">Parameters</span></span>

<span data-ttu-id="26c3a-109">\[in \] uv : puntatore a un vettore che contiene la coordinata della trama dei vertici.</span><span class="sxs-lookup"><span data-stu-id="26c3a-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="26c3a-110">\[in uPrimitiveId: indice del triangolo di input nella mesh per cui deve essere calcolato \] il segnale.</span><span class="sxs-lookup"><span data-stu-id="26c3a-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="26c3a-111">\[in \] uSignalDimension: numero di valori float da archiviare nella matrice di dati del segnale (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="26c3a-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="26c3a-112">\[in \] pUserData: puntatore pUserData passato a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="26c3a-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="26c3a-113">\[out \] pfSignalOut: matrice di valori float che contiene i dati del segnale.</span><span class="sxs-lookup"><span data-stu-id="26c3a-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="26c3a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26c3a-114">Return Value</span></span>

<span data-ttu-id="26c3a-115">Questa funzione deve essere implementata per restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26c3a-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="26c3a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="26c3a-116">Remarks</span></span>

<span data-ttu-id="26c3a-117">Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="26c3a-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="26c3a-118">In caso contrario, possono verificarsi overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="26c3a-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="26c3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c3a-119">Requirement</span></span>               | <span data-ttu-id="26c3a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="26c3a-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="26c3a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26c3a-121">Header</span></span>         | <span data-ttu-id="26c3a-122">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="26c3a-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="26c3a-123">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="26c3a-123">Import Library</span></span> | <span data-ttu-id="26c3a-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="26c3a-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="26c3a-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26c3a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26c3a-126">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="26c3a-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
