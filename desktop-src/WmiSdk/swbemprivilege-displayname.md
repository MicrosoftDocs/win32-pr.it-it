---
description: La proprietà DisplayName di un oggetto SWbemPrivilege è una stringa che visualizza una descrizione di un oggetto SWbemPrivilege.
ms.assetid: 9ed91a6a-e513-4a72-b8a9-3180e42b811f
ms.tgt_platform: multiple
title: Proprietà SWbemPrivilege. DisplayName (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.DisplayName
- ISWbemPrivilege.DisplayName
- ISWbemPrivilege.get_DisplayName
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bb45bdce52b1930f1893f7716d573033627e0cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309800"
---
# <a name="swbemprivilegedisplayname-property"></a><span data-ttu-id="4a7ef-103">Proprietà SWbemPrivilege. DisplayName</span><span class="sxs-lookup"><span data-stu-id="4a7ef-103">SWbemPrivilege.DisplayName property</span></span>

<span data-ttu-id="4a7ef-104">La proprietà **DisplayName** di un oggetto [**SWbemPrivilege**](swbemprivilege.md) è una stringa che visualizza una descrizione di un oggetto **SWbemPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="4a7ef-104">The **DisplayName** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that displays a description of an **SWbemPrivilege** object.</span></span> <span data-ttu-id="4a7ef-105">Ad esempio, il privilegio che controlla se un utente può eseguire il metodo Shutdown di un oggetto ha la stringa "arresta il sistema" nella proprietà **SWbemPrivilege. DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="4a7ef-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "Shut down the system" string in the **SWbemPrivilege.DisplayName** property.</span></span> <span data-ttu-id="4a7ef-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4a7ef-106">This property is read-only.</span></span>

<span data-ttu-id="4a7ef-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4a7ef-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="4a7ef-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4a7ef-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a7ef-109">Syntax</span></span>


```VB
SWbemPrivilege.DisplayName As 
```



## <a name="property-value"></a><span data-ttu-id="4a7ef-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4a7ef-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7ef-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a7ef-111">Requirements</span></span>



| <span data-ttu-id="4a7ef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a7ef-112">Requirement</span></span> | <span data-ttu-id="4a7ef-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4a7ef-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7ef-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a7ef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7ef-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a7ef-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a7ef-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a7ef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7ef-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a7ef-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a7ef-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a7ef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7ef-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7ef-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a7ef-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4a7ef-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a7ef-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a7ef-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a7ef-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4a7ef-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a7ef-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a7ef-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a7ef-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a7ef-124">CLSID</span></span><br/>                    | <span data-ttu-id="4a7ef-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="4a7ef-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="4a7ef-126">IID</span><span class="sxs-lookup"><span data-stu-id="4a7ef-126">IID</span></span><br/>                      | <span data-ttu-id="4a7ef-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="4a7ef-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




