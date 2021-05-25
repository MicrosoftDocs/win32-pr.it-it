---
description: Funzione di callback per UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342796"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="3b809-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="3b809-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="3b809-104">Funzione di callback per UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="3b809-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b809-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b809-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="3b809-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b809-106">Parameters</span></span>

<span data-ttu-id="3b809-107">\[out fPercentDone: numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati \] (tra 0 e 100%).</span><span class="sxs-lookup"><span data-stu-id="3b809-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="3b809-108">\[in lpUserContext: puntatore a un valore definito dall'utente passato alla funzione di callback; in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione \] di callback.</span><span class="sxs-lookup"><span data-stu-id="3b809-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b809-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b809-109">Return Value</span></span>

<span data-ttu-id="3b809-110">Questa funzione deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore.</span><span class="sxs-lookup"><span data-stu-id="3b809-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="3b809-111">Qualsiasi altro valore interromperà il simulatore.</span><span class="sxs-lookup"><span data-stu-id="3b809-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b809-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b809-112">Remarks</span></span>

<span data-ttu-id="3b809-113">Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="3b809-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="3b809-114">In caso contrario, possono verificarsi overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="3b809-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="3b809-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b809-115">Requirement</span></span>                         | <span data-ttu-id="3b809-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b809-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="3b809-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b809-117">Header</span></span>                   | <span data-ttu-id="3b809-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="3b809-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="3b809-119">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="3b809-119">Import Library</span></span>           | <span data-ttu-id="3b809-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="3b809-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="3b809-121">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="3b809-121">Minimum Operating System</span></span> | <span data-ttu-id="3b809-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3b809-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3b809-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b809-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b809-124">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="3b809-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
