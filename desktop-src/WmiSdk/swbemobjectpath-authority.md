---
description: La proprietà Authority dell'oggetto SWbemObjectPath contiene una stringa che definisce il componente Authority del percorso dell'oggetto.
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Authority (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318511"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="1055d-103">Proprietà SWbemObjectPath. Authority</span><span class="sxs-lookup"><span data-stu-id="1055d-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="1055d-104">La proprietà **Authority** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene una stringa che definisce il componente Authority del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1055d-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="1055d-105">Per ulteriori informazioni, vedere il parametro *strAuthority* del metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="1055d-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="1055d-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1055d-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1055d-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1055d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1055d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1055d-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="1055d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1055d-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="1055d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1055d-110">Requirements</span></span>



| <span data-ttu-id="1055d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1055d-111">Requirement</span></span> | <span data-ttu-id="1055d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1055d-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1055d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1055d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1055d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1055d-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1055d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1055d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1055d-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1055d-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1055d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1055d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1055d-118"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1055d-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1055d-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1055d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1055d-120"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1055d-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1055d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1055d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1055d-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1055d-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1055d-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="1055d-123">CLSID</span></span><br/>                    | <span data-ttu-id="1055d-124">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="1055d-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="1055d-125">IID</span><span class="sxs-lookup"><span data-stu-id="1055d-125">IID</span></span><br/>                      | <span data-ttu-id="1055d-126">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="1055d-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




