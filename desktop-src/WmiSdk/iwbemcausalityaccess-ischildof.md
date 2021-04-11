---
description: Il metodo IsChildOf determina se una richiesta è un elemento figlio di una richiesta specificata (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Metodo IWbemCausalityAccess:: IsChildOf (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232623"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="e3406-103">Metodo IWbemCausalityAccess:: IsChildOf</span><span class="sxs-lookup"><span data-stu-id="e3406-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="e3406-104">Il metodo **IsChildOf** determina se una richiesta è un elemento figlio di una richiesta specificata (PID).</span><span class="sxs-lookup"><span data-stu-id="e3406-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="e3406-105">Una richiesta padre può avere più richieste figlio.</span><span class="sxs-lookup"><span data-stu-id="e3406-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="e3406-106">Ogni richiesta viene identificata da un identificatore univoco globale (GUID) e può disporre di una richiesta padre oppure può essere una richiesta top.</span><span class="sxs-lookup"><span data-stu-id="e3406-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="e3406-107">Un GUID è un numero univoco a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="e3406-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3406-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3406-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="e3406-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3406-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3406-110">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3406-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3406-111">Valore GUID che identifica in modo univoco una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e3406-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="e3406-112">Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="e3406-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3406-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3406-113">Return value</span></span>

<span data-ttu-id="e3406-114">Restituisce esito positivo se la richiesta specificata è un elemento figlio della richiesta che chiama il metodo **IsChildOf** .</span><span class="sxs-lookup"><span data-stu-id="e3406-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3406-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3406-115">Requirements</span></span>



| <span data-ttu-id="e3406-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3406-116">Requirement</span></span> | <span data-ttu-id="e3406-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e3406-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3406-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3406-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3406-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3406-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3406-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3406-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3406-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3406-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3406-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3406-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3406-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3406-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="e3406-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e3406-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3406-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3406-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3406-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3406-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3406-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="e3406-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




