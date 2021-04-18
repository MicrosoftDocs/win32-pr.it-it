---
description: La proprietà ConfigurableItems di sola lettura dell'oggetto merge restituisce una raccolta di oggetti ConfigurableItem, ognuno dei quali rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Proprietà Merge.ConfigurableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327323"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="4808d-103">Merge.Configproprietà urableItems</span><span class="sxs-lookup"><span data-stu-id="4808d-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="4808d-104">La proprietà **ConfigurableItems** di sola lettura dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**ConfigurableItem**](configurableitem-object.md) , ognuno dei quali rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="4808d-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="4808d-105">Semanticamente, ogni interfaccia nell'enumeratore rappresenta un elemento che può essere configurato dall'utente del modulo.</span><span class="sxs-lookup"><span data-stu-id="4808d-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="4808d-106">La raccolta è una raccolta di sola lettura e implementa le interfacce di raccolta di sola lettura standard di Item (), Count () e \_ NewEnum ().</span><span class="sxs-lookup"><span data-stu-id="4808d-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="4808d-107">L'enumeratore **IEnumMsmConfigItems** implementa Next (), Skip (), Reset () e Clone () con la semantica standard.</span><span class="sxs-lookup"><span data-stu-id="4808d-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="4808d-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4808d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4808d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4808d-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="4808d-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4808d-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="4808d-111">C++</span><span class="sxs-lookup"><span data-stu-id="4808d-111">C++</span></span>

<span data-ttu-id="4808d-112">Vedere [**ottenere \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) la funzione ConfigurableItems.</span><span class="sxs-lookup"><span data-stu-id="4808d-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4808d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4808d-113">Requirements</span></span>



| <span data-ttu-id="4808d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4808d-114">Requirement</span></span> | <span data-ttu-id="4808d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4808d-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4808d-116">Versione</span><span class="sxs-lookup"><span data-stu-id="4808d-116">Version</span></span><br/> | <span data-ttu-id="4808d-117">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4808d-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="4808d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4808d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4808d-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="4808d-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="4808d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4808d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4808d-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4808d-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




