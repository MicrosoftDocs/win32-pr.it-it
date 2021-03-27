---
description: Espone i metodi usati per inizializzare un elenco usato più di recente (MRU) per un oggetto di completamento automatico.
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
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994624"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="8b92b-103">Interfaccia IACLCustomMRU</span><span class="sxs-lookup"><span data-stu-id="8b92b-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="8b92b-104">Espone i metodi usati per inizializzare un elenco usato più di recente (MRU) per un oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="8b92b-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="8b92b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="8b92b-105">Members</span></span>

<span data-ttu-id="8b92b-106">L'interfaccia **IACLCustomMRU** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b92b-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b92b-107">**IACLCustomMRU** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8b92b-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="8b92b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="8b92b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b92b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="8b92b-109">Methods</span></span>

<span data-ttu-id="8b92b-110">L'interfaccia **IACLCustomMRU** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8b92b-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="8b92b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="8b92b-111">Method</span></span>                                             | <span data-ttu-id="8b92b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b92b-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="8b92b-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="8b92b-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="8b92b-114">Aggiunge una voce all'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="8b92b-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="8b92b-115">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="8b92b-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="8b92b-116">Carica un elenco di stringhe nell'elenco MRU dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8b92b-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b92b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b92b-117">Requirements</span></span>



| <span data-ttu-id="8b92b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b92b-118">Requirement</span></span> | <span data-ttu-id="8b92b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8b92b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b92b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b92b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b92b-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b92b-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8b92b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b92b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b92b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b92b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
