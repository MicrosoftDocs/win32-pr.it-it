---
description: Il metodo SWbemRefresher. Refresh aggiorna tutti gli elementi contenuti nell'oggetto SWbemRefresher. Oggetto SWbemRefresher.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Refresh (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320582"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="6896e-103">Metodo SWbemRefresher. Refresh</span><span class="sxs-lookup"><span data-stu-id="6896e-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="6896e-104">Il metodo **SWbemRefresher. Refresh** Aggiorna tutti gli elementi contenuti nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="6896e-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="6896e-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6896e-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6896e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6896e-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6896e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6896e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6896e-108">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="6896e-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6896e-109">I flag devono essere impostati su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6896e-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6896e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6896e-110">Return value</span></span>

<span data-ttu-id="6896e-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6896e-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6896e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6896e-112">Requirements</span></span>



| <span data-ttu-id="6896e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6896e-113">Requirement</span></span> | <span data-ttu-id="6896e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6896e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6896e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6896e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6896e-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6896e-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6896e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6896e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6896e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6896e-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6896e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6896e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6896e-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6896e-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6896e-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6896e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6896e-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6896e-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6896e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6896e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6896e-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6896e-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6896e-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="6896e-125">CLSID</span></span><br/>                    | <span data-ttu-id="6896e-126">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="6896e-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="6896e-127">IID</span><span class="sxs-lookup"><span data-stu-id="6896e-127">IID</span></span><br/>                      | <span data-ttu-id="6896e-128">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="6896e-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="6896e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6896e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6896e-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="6896e-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




