---
description: Il \_ messaggio di riga QUEUESTATUS viene inviato quando lo stato di una coda ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Messaggio di LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328909"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="0174c-104">\_Messaggio linea QUEUESTATUS</span><span class="sxs-lookup"><span data-stu-id="0174c-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="0174c-105">Il messaggio di **riga \_ QUEUESTATUS** viene inviato quando lo stato di una coda ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta.</span><span class="sxs-lookup"><span data-stu-id="0174c-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="0174c-106">Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="0174c-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="0174c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0174c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0174c-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="0174c-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-109">Handle dell'applicazione per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="0174c-109">The application's handle to the line device.</span></span> <span data-ttu-id="0174c-110">Questo si riferisce al gestore agenti.</span><span class="sxs-lookup"><span data-stu-id="0174c-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="0174c-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="0174c-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="0174c-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="0174c-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0174c-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-114">Identificatore della coda il cui stato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="0174c-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0174c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0174c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-116">Specifica lo stato della coda che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="0174c-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="0174c-117">Può essere una o più delle [**\_ costanti LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="0174c-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0174c-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0174c-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0174c-119">Reserved.</span></span> <span data-ttu-id="0174c-120">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="0174c-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0174c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0174c-121">Requirements</span></span>



| <span data-ttu-id="0174c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0174c-122">Requirement</span></span> | <span data-ttu-id="0174c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0174c-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0174c-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0174c-124">TAPI version</span></span><br/> | <span data-ttu-id="0174c-125">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0174c-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="0174c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0174c-126">Header</span></span><br/>       | <dl> <span data-ttu-id="0174c-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0174c-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0174c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0174c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0174c-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="0174c-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




