---
description: Funzione di callback per la simulazione e la compressione dei PRT (pre-Computed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482085"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="9d946-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="9d946-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="9d946-104">Funzione di callback per la simulazione e la compressione dei PRT (pre-Computed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="9d946-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d946-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d946-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="9d946-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d946-106">Parameters</span></span>

<span data-ttu-id="9d946-107">fPercentDone: numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (compreso tra 0 e 100%).</span><span class="sxs-lookup"><span data-stu-id="9d946-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="9d946-108">lpUserContext: puntatore a un valore definito dall'utente che viene passato alla funzione di callback. usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="9d946-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d946-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d946-109">Return Value</span></span>

<span data-ttu-id="9d946-110">Questa funzione deve essere implementata per restituire S \_ OK per tenere in esecuzione il simulatore.</span><span class="sxs-lookup"><span data-stu-id="9d946-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="9d946-111">Qualsiasi altro valore arresterà il simulatore.</span><span class="sxs-lookup"><span data-stu-id="9d946-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d946-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d946-112">Remarks</span></span>

<span data-ttu-id="9d946-113">Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="9d946-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="9d946-114">In caso contrario, è possibile che si verifichino overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="9d946-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="9d946-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d946-115">Header</span></span>                   | <span data-ttu-id="9d946-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="9d946-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="9d946-117">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="9d946-117">Import Library</span></span>           | <span data-ttu-id="9d946-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="9d946-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="9d946-119">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="9d946-119">Minimum Operating System</span></span> | <span data-ttu-id="9d946-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9d946-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="9d946-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d946-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d946-122">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="9d946-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
