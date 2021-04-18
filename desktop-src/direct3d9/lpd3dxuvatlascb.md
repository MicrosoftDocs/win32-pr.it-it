---
description: Funzione di callback per UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304094"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="b1d9f-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="b1d9f-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="b1d9f-104">Funzione di callback per UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d9f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1d9f-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="b1d9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1d9f-106">Parameters</span></span>

<span data-ttu-id="b1d9f-107">\[out \] fPercentDone-numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (compreso tra 0 e 100%).</span><span class="sxs-lookup"><span data-stu-id="b1d9f-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="b1d9f-108">\[in \] lpUserContext-puntatore a un valore definito dall'utente che viene passato alla funzione di callback; in genere utilizzato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1d9f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1d9f-109">Return Value</span></span>

<span data-ttu-id="b1d9f-110">Questa funzione deve essere implementata per restituire S \_ OK per tenere in esecuzione il simulatore.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="b1d9f-111">Qualsiasi altro valore arresterà il simulatore.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d9f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1d9f-112">Remarks</span></span>

<span data-ttu-id="b1d9f-113">Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="b1d9f-114">In caso contrario, è possibile che si verifichino overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="b1d9f-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="b1d9f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1d9f-115">Header</span></span>                   | <span data-ttu-id="b1d9f-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="b1d9f-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="b1d9f-117">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="b1d9f-117">Import Library</span></span>           | <span data-ttu-id="b1d9f-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="b1d9f-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="b1d9f-119">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="b1d9f-119">Minimum Operating System</span></span> | <span data-ttu-id="b1d9f-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b1d9f-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="b1d9f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1d9f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d9f-122">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="b1d9f-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
