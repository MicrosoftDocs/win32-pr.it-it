---
description: Il messaggio di riga \_ GROUPSTATUS viene inviato quando lo stato di un gruppo ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Messaggio di LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327406"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="4c869-104">\_Messaggio linea GROUPSTATUS</span><span class="sxs-lookup"><span data-stu-id="4c869-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="4c869-105">Il messaggio di **riga \_ GROUPSTATUS** viene inviato quando lo stato di un gruppo ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta.</span><span class="sxs-lookup"><span data-stu-id="4c869-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="4c869-106">Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="4c869-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="4c869-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c869-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c869-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="4c869-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4c869-109">Handle dell'applicazione per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="4c869-109">The application's handle to the line device.</span></span> <span data-ttu-id="4c869-110">Questo si riferisce al gestore agenti.</span><span class="sxs-lookup"><span data-stu-id="4c869-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="4c869-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4c869-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4c869-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="4c869-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="4c869-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4c869-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4c869-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4c869-114">Reserved.</span></span> <span data-ttu-id="4c869-115">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="4c869-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c869-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4c869-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4c869-117">Specifica lo stato del gruppo che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="4c869-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="4c869-118">L'applicazione può richiamare [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) per determinare le modifiche nei gruppi disponibili.</span><span class="sxs-lookup"><span data-stu-id="4c869-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="4c869-119">Il parametro *dwParam2* è una o più [**\_ costanti LINEGROUPSTATUS**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="4c869-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c869-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4c869-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4c869-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4c869-121">Reserved.</span></span> <span data-ttu-id="4c869-122">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="4c869-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c869-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c869-123">Requirements</span></span>



| <span data-ttu-id="4c869-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c869-124">Requirement</span></span> | <span data-ttu-id="4c869-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4c869-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c869-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="4c869-126">TAPI version</span></span><br/> | <span data-ttu-id="4c869-127">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="4c869-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4c869-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c869-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4c869-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c869-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c869-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c869-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c869-131">**lineGetGroupList**</span><span class="sxs-lookup"><span data-stu-id="4c869-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




