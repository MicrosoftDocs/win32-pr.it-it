---
description: La proprietà di sola lettura dipendenze dell'oggetto merge restituisce una raccolta di oggetti dipendenza che enumera un set di dipendenze non soddisfatte per il database corrente.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Proprietà merge. dipendenze (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327806"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="e9d75-103">Merge. dipendenze (proprietà)</span><span class="sxs-lookup"><span data-stu-id="e9d75-103">Merge.Dependencies property</span></span>

<span data-ttu-id="e9d75-104">La proprietà di sola lettura **dipendenze** dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**dipendenza**](dependency-object.md) che enumera un set di dipendenze non soddisfatte per il database corrente.</span><span class="sxs-lookup"><span data-stu-id="e9d75-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="e9d75-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9d75-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d75-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9d75-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="e9d75-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e9d75-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d75-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9d75-108">Remarks</span></span>

<span data-ttu-id="e9d75-109">Non è necessario che un modulo sia aperto per recuperare le informazioni sulle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="e9d75-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="e9d75-110">C++</span><span class="sxs-lookup"><span data-stu-id="e9d75-110">C++</span></span>

<span data-ttu-id="e9d75-111">Vedere ottenere la funzione delle [**\_ dipendenze**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .</span><span class="sxs-lookup"><span data-stu-id="e9d75-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d75-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9d75-112">Requirements</span></span>



| <span data-ttu-id="e9d75-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9d75-113">Requirement</span></span> | <span data-ttu-id="e9d75-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e9d75-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d75-115">Versione</span><span class="sxs-lookup"><span data-stu-id="e9d75-115">Version</span></span><br/> | <span data-ttu-id="e9d75-116">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e9d75-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e9d75-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9d75-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9d75-118"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9d75-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9d75-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d75-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9d75-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d75-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
