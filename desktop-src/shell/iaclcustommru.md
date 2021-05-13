---
description: Espone i metodi utilizzati per inizializzare un elenco degli elementi usati più di recente per un oggetto di completamento automatico.
title: Interfaccia IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: f47a9df320da5c710c21ddbab83ca87b49c28e12
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842012"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="bd28d-103">Interfaccia IACLCustomMRU</span><span class="sxs-lookup"><span data-stu-id="bd28d-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="bd28d-104">Espone i metodi utilizzati per inizializzare un elenco degli elementi usati più di recente per un oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="bd28d-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="bd28d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="bd28d-105">Members</span></span>

<span data-ttu-id="bd28d-106">**L'interfaccia IACLCustomMRU** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="bd28d-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd28d-107">**IACLCustomMRU** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bd28d-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="bd28d-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="bd28d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd28d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="bd28d-109">Methods</span></span>

<span data-ttu-id="bd28d-110">**L'interfaccia IACLCustomMRU** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bd28d-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="bd28d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="bd28d-111">Method</span></span>                                             | <span data-ttu-id="bd28d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd28d-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="bd28d-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="bd28d-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="bd28d-114">Aggiunge una voce all'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="bd28d-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="bd28d-115">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="bd28d-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="bd28d-116">Carica un elenco di stringhe nell'elenco MRU dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bd28d-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd28d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd28d-117">Requirements</span></span>



| <span data-ttu-id="bd28d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd28d-118">Requirement</span></span> | <span data-ttu-id="bd28d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bd28d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bd28d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd28d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd28d-121">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bd28d-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bd28d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd28d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd28d-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd28d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
