---
description: Il messaggio della linea TAPI \_ CALLHUBCLOSE viene inviato quando un hub di chiamata è stato chiuso.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Messaggio di LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328053"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="0332c-103">\_Messaggio linea CALLHUBCLOSE</span><span class="sxs-lookup"><span data-stu-id="0332c-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="0332c-104">Il messaggio della **linea TAPI \_ CALLHUBCLOSE** viene inviato quando un hub di chiamata è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="0332c-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="0332c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0332c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0332c-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="0332c-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0332c-107">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="0332c-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="0332c-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="0332c-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0332c-109">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="0332c-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="0332c-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0332c-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0332c-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0332c-111">Reserved.</span></span> <span data-ttu-id="0332c-112">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="0332c-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0332c-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0332c-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0332c-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0332c-114">Reserved.</span></span> <span data-ttu-id="0332c-115">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="0332c-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0332c-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0332c-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0332c-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0332c-117">Reserved.</span></span> <span data-ttu-id="0332c-118">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="0332c-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0332c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0332c-119">Return value</span></span>

<span data-ttu-id="0332c-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="0332c-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0332c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0332c-121">Remarks</span></span>

<span data-ttu-id="0332c-122">Questo messaggio ha origine con TAPI anziché con un provider di servizi, pertanto non esiste alcun messaggio TSPI corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0332c-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0332c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0332c-123">Requirements</span></span>



| <span data-ttu-id="0332c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0332c-124">Requirement</span></span> | <span data-ttu-id="0332c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0332c-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0332c-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0332c-126">TAPI version</span></span><br/> | <span data-ttu-id="0332c-127">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0332c-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="0332c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0332c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="0332c-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0332c-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




