---
title: Proprietà TaskNamedValueCollection. Item
description: Per gli script, ottiene la coppia nome-valore specificata dalla raccolta.
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto TaskNamedValueCollection
- Oggetto TaskNamedValueCollection Utilità di pianificazione, proprietà Item
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd0abff47d699fd6d85f04745f28e2feb31c6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302224"
---
# <a name="tasknamedvaluecollectionitem-property"></a><span data-ttu-id="81695-106">Proprietà TaskNamedValueCollection. Item</span><span class="sxs-lookup"><span data-stu-id="81695-106">TaskNamedValueCollection.Item property</span></span>

<span data-ttu-id="81695-107">Per gli script, ottiene la coppia nome-valore specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="81695-107">For scripting, gets the specified name-value pair from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81695-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81695-108">Syntax</span></span>


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a><span data-ttu-id="81695-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="81695-109">Property value</span></span>

<span data-ttu-id="81695-110">Oggetto [**TaskNamedValuePair**](tasknamedvaluepair.md) che rappresenta la coppia richiesta.</span><span class="sxs-lookup"><span data-stu-id="81695-110">A [**TaskNamedValuePair**](tasknamedvaluepair.md) object that represents the requested pair.</span></span>

## <a name="requirements"></a><span data-ttu-id="81695-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81695-111">Requirements</span></span>



| <span data-ttu-id="81695-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="81695-112">Requirement</span></span> | <span data-ttu-id="81695-113">Valore</span><span class="sxs-lookup"><span data-stu-id="81695-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81695-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81695-114">Minimum supported client</span></span><br/> | <span data-ttu-id="81695-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81695-115">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="81695-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81695-116">Minimum supported server</span></span><br/> | <span data-ttu-id="81695-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81695-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81695-118">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="81695-118">Type library</span></span><br/>             | <dl> <span data-ttu-id="81695-119"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81695-119"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81695-120">DLL</span><span class="sxs-lookup"><span data-stu-id="81695-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81695-121"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81695-121"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





