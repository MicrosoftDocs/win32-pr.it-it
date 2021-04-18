---
title: Funzione CommandListCast (D3dx12. h)
description: Questo modello di funzione esegue il cast di un puntatore costante a un elenco di comandi in un puntatore const a un ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast (funzione)
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323430"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="700f7-104">CommandListCast (funzione)</span><span class="sxs-lookup"><span data-stu-id="700f7-104">CommandListCast function</span></span>

<span data-ttu-id="700f7-105">Questo modello di funzione esegue il cast di un puntatore costante a un elenco di comandi in un puntatore const a un ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="700f7-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="700f7-106">Questo cast è utile per passare puntatori di elenchi di comandi fortemente tipizzati in [**oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="700f7-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="700f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="700f7-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="700f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="700f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700f7-109">*PP*</span><span class="sxs-lookup"><span data-stu-id="700f7-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="700f7-110">Tipo: **t \_ CommandListType \* const \***</span><span class="sxs-lookup"><span data-stu-id="700f7-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="700f7-111">Elenco di comandi fortemente tipizzati di cui eseguire il cast.</span><span class="sxs-lookup"><span data-stu-id="700f7-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="700f7-112">L'argomento di modello **t \_ CommandListType** specifica un oggetto elenco di comandi fortemente tipizzato.</span><span class="sxs-lookup"><span data-stu-id="700f7-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700f7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="700f7-113">Return value</span></span>

<span data-ttu-id="700f7-114">Tipo: **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="700f7-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="700f7-115">Elenco di comandi fortemente tipizzati, reinterpretato come un [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="700f7-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="700f7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="700f7-116">Remarks</span></span>

<span data-ttu-id="700f7-117">CommandListCast esegue un **\_ cast di reinterpretazione**.</span><span class="sxs-lookup"><span data-stu-id="700f7-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="700f7-118">Il cast è valido finché viene rispettata la const dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="700f7-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="700f7-119">La funzione CommandListCast è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="700f7-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="700f7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700f7-120">Requirements</span></span>



| <span data-ttu-id="700f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="700f7-121">Requirement</span></span> | <span data-ttu-id="700f7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="700f7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="700f7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="700f7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="700f7-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="700f7-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="700f7-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="700f7-125">Library</span></span><br/> | <dl> <span data-ttu-id="700f7-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="700f7-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="700f7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="700f7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="700f7-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="700f7-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700f7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700f7-130">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="700f7-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





