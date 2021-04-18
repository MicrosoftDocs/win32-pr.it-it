---
description: Prototipo di funzione usato da D3DXComputeIMTFromSignal per descrivere un segnale definito dall'utente nello spazio u, v della mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension alla coordinata u, v specificata.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303676"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="ca8c0-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="ca8c0-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="ca8c0-105">Prototipo di funzione usato da [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) per descrivere un segnale definito dall'utente nello spazio u, v della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="ca8c0-106">La funzione valuta un segnale procedurale della dimensione uSignalDimension alla coordinata u, v specificata.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8c0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca8c0-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="ca8c0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca8c0-108">Parameters</span></span>

<span data-ttu-id="ca8c0-109">\[in un \] puntatore UV a un vettore che contiene la coordinata di trama del vertice.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="ca8c0-110">\[in \] uPrimitiveId: Indice del triangolo di input sulla mesh per cui deve essere calcolato il segnale.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="ca8c0-111">\[in \] uSignalDimension: numero di float da archiviare nella matrice di dati del segnale (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="ca8c0-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="ca8c0-112">\[in \] pUserData-il puntatore pUserData passato a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="ca8c0-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="ca8c0-113">\[out \] pfSignalOut: matrice di float, che contiene i dati del segnale.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca8c0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca8c0-114">Return Value</span></span>

<span data-ttu-id="ca8c0-115">Questa funzione deve essere implementata per restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca8c0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca8c0-116">Remarks</span></span>

<span data-ttu-id="ca8c0-117">Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="ca8c0-118">In caso contrario, è possibile che si verifichino overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="ca8c0-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="ca8c0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca8c0-119">Header</span></span>         | <span data-ttu-id="ca8c0-120">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="ca8c0-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="ca8c0-121">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="ca8c0-121">Import Library</span></span> | <span data-ttu-id="ca8c0-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="ca8c0-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="ca8c0-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca8c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca8c0-124">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="ca8c0-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
