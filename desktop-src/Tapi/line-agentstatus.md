---
description: Il messaggio della linea TAPI \_ AGENTSTATUS viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAgentStatus per determinare lo stato corrente dell'agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Messaggio di LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331038"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="88a89-104">\_Messaggio linea AGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="88a89-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="88a89-105">Il messaggio della **linea TAPI \_ AGENTSTATUS** viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88a89-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="88a89-106">L'applicazione può richiamare [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) per determinare lo stato corrente dell'agente.</span><span class="sxs-lookup"><span data-stu-id="88a89-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="88a89-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="88a89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a89-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="88a89-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="88a89-109">Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato dell'agente.</span><span class="sxs-lookup"><span data-stu-id="88a89-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="88a89-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="88a89-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="88a89-111">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="88a89-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="88a89-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="88a89-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="88a89-113">Identificatore dell'indirizzo sulla riga in cui è stato modificato lo stato dell'agente.</span><span class="sxs-lookup"><span data-stu-id="88a89-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="88a89-114">Un identificatore di indirizzo è associato in modo permanente a un indirizzo. l'identificatore rimane costante tra gli aggiornamenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="88a89-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="88a89-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="88a89-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="88a89-116">Specifica lo stato dell'agente che è stato modificato. può essere una combinazione di [**\_ costanti LINEAGENTSTATUS**](lineagentstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="88a89-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="88a89-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="88a89-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="88a89-118">Se *dwParam2* include il \_ bit di stato LINEAGENTSTATUS, *dwParam3* indica il nuovo valore del membro **dwState** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span><span class="sxs-lookup"><span data-stu-id="88a89-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="88a89-119">In caso contrario, questo parametro è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="88a89-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a89-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88a89-120">Return value</span></span>

<span data-ttu-id="88a89-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="88a89-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a89-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="88a89-122">Remarks</span></span>

<span data-ttu-id="88a89-123">Il messaggio di **riga \_ AGENTSTATUS** non viene inviato ad applicazioni che supportano le versioni precedenti di TAPI.</span><span class="sxs-lookup"><span data-stu-id="88a89-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a89-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88a89-124">Requirements</span></span>



| <span data-ttu-id="88a89-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88a89-125">Requirement</span></span> | <span data-ttu-id="88a89-126">Valore</span><span class="sxs-lookup"><span data-stu-id="88a89-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88a89-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="88a89-127">TAPI version</span></span><br/> | <span data-ttu-id="88a89-128">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="88a89-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="88a89-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88a89-129">Header</span></span><br/>       | <dl> <span data-ttu-id="88a89-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="88a89-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88a89-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88a89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a89-132">**LINEAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="88a89-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="88a89-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="88a89-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




