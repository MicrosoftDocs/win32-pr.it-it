---
description: La proprietà Format dell'oggetto ConfigurableItem restituisce il valore della colonna Format della tabella ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Proprietà ConfigurableItem. Format (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328071"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="fb396-103">Proprietà ConfigurableItem. Format</span><span class="sxs-lookup"><span data-stu-id="fb396-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="fb396-104">La proprietà **Format** dell'oggetto [**ConfigurableItem**](configurableitem-object.md) restituisce il valore della colonna Format della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb396-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="fb396-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb396-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb396-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb396-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="fb396-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb396-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="fb396-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb396-108">Remarks</span></span>

<span data-ttu-id="fb396-109">Questa proprietà può avere solo i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb396-109">This property can only have the following values.</span></span>



| <span data-ttu-id="fb396-110">Costante</span><span class="sxs-lookup"><span data-stu-id="fb396-110">Constant</span></span>                        | <span data-ttu-id="fb396-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fb396-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="fb396-112">**msmConfigurableItemText**</span><span class="sxs-lookup"><span data-stu-id="fb396-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="fb396-113">0</span><span class="sxs-lookup"><span data-stu-id="fb396-113">0</span></span>     |
| <span data-ttu-id="fb396-114">**msmConfigurableItemKey**</span><span class="sxs-lookup"><span data-stu-id="fb396-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="fb396-115">1</span><span class="sxs-lookup"><span data-stu-id="fb396-115">1</span></span>     |
| <span data-ttu-id="fb396-116">**msmConfigurableItemInteger**</span><span class="sxs-lookup"><span data-stu-id="fb396-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="fb396-117">2</span><span class="sxs-lookup"><span data-stu-id="fb396-117">2</span></span>     |
| <span data-ttu-id="fb396-118">**msmConfigurableItemBitfield**</span><span class="sxs-lookup"><span data-stu-id="fb396-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="fb396-119">3</span><span class="sxs-lookup"><span data-stu-id="fb396-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="fb396-120">C++</span><span class="sxs-lookup"><span data-stu-id="fb396-120">C++</span></span>

<span data-ttu-id="fb396-121">Vedere [**ottenere \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) la funzione Format.</span><span class="sxs-lookup"><span data-stu-id="fb396-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb396-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb396-122">Requirements</span></span>



| <span data-ttu-id="fb396-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb396-123">Requirement</span></span> | <span data-ttu-id="fb396-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fb396-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb396-125">Versione</span><span class="sxs-lookup"><span data-stu-id="fb396-125">Version</span></span><br/> | <span data-ttu-id="fb396-126">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fb396-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="fb396-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb396-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fb396-128"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb396-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb396-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fb396-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb396-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb396-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




