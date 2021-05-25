---
description: Funzione di callback per la simulazione e la compressione PRT (Precomputed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342806"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="e6311-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="e6311-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="e6311-104">Funzione di callback per la simulazione e la compressione PRT (Precomputed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="e6311-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6311-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6311-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="e6311-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6311-106">Parameters</span></span>

<span data-ttu-id="e6311-107">fPercentDone : numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (tra 0 e 100%).</span><span class="sxs-lookup"><span data-stu-id="e6311-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="e6311-108">lpUserContext: puntatore a un valore definito dall'utente passato alla funzione di callback. in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e6311-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6311-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6311-109">Return Value</span></span>

<span data-ttu-id="e6311-110">Questa funzione deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore.</span><span class="sxs-lookup"><span data-stu-id="e6311-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="e6311-111">Qualsiasi altro valore arresterà il simulatore.</span><span class="sxs-lookup"><span data-stu-id="e6311-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6311-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6311-112">Remarks</span></span>

<span data-ttu-id="e6311-113">Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e6311-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e6311-114">In caso contrario, possono verificarsi overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="e6311-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="e6311-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6311-115">Requirement</span></span>                         | <span data-ttu-id="e6311-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e6311-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="e6311-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6311-117">Header</span></span>                   | <span data-ttu-id="e6311-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="e6311-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="e6311-119">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="e6311-119">Import Library</span></span>           | <span data-ttu-id="e6311-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="e6311-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="e6311-121">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="e6311-121">Minimum Operating System</span></span> | <span data-ttu-id="e6311-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e6311-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e6311-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6311-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6311-124">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="e6311-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
