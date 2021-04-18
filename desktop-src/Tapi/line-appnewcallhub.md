---
description: Il messaggio della linea TAPI \_ APPNEWCALLHUB viene inviato per informare un'applicazione quando è stato creato un nuovo hub di chiamata.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Messaggio di LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331033"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="04e80-103">\_Messaggio linea APPNEWCALLHUB</span><span class="sxs-lookup"><span data-stu-id="04e80-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="04e80-104">Il messaggio della **linea TAPI \_ APPNEWCALLHUB** viene inviato per informare un'applicazione quando è stato creato un nuovo hub di chiamata.</span><span class="sxs-lookup"><span data-stu-id="04e80-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="04e80-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="04e80-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e80-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="04e80-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="04e80-107">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="04e80-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="04e80-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="04e80-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="04e80-109">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="04e80-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="04e80-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="04e80-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="04e80-111">Livello di rilevamento sul nuovo hub, come definito da una delle [**\_ costanti LINECALLHUBTRACKING**](linecallhubtracking--constants.md).</span><span class="sxs-lookup"><span data-stu-id="04e80-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e80-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04e80-112">Return value</span></span>

<span data-ttu-id="04e80-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="04e80-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e80-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="04e80-114">Remarks</span></span>

<span data-ttu-id="04e80-115">Questo messaggio ha origine con TAPI anziché con un provider di servizi, pertanto non esiste alcun messaggio TSPI corrispondente.</span><span class="sxs-lookup"><span data-stu-id="04e80-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e80-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04e80-116">Requirements</span></span>



| <span data-ttu-id="04e80-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e80-117">Requirement</span></span> | <span data-ttu-id="04e80-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04e80-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="04e80-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="04e80-119">TAPI version</span></span><br/> | <span data-ttu-id="04e80-120">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="04e80-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="04e80-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04e80-121">Header</span></span><br/>       | <dl> <span data-ttu-id="04e80-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e80-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




