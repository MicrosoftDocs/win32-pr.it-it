---
description: Il \_ messaggio Creazione linea TAPI viene inviato per informare l'applicazione della creazione di un nuovo dispositivo a linee.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Messaggio di LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328127"
---
# <a name="line_create-message"></a><span data-ttu-id="e2847-103">\_Creazione riga messaggio</span><span class="sxs-lookup"><span data-stu-id="e2847-103">LINE\_CREATE message</span></span>

<span data-ttu-id="e2847-104">Il messaggio **\_ creazione linea** TAPI viene inviato per informare l'applicazione della creazione di un nuovo dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="e2847-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e2847-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2847-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2847-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="e2847-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e2847-107">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e2847-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e2847-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e2847-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e2847-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e2847-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e2847-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e2847-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e2847-111">*HDeviceID* del dispositivo appena creato.</span><span class="sxs-lookup"><span data-stu-id="e2847-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="e2847-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e2847-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e2847-113">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e2847-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e2847-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e2847-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e2847-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e2847-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2847-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2847-116">Return value</span></span>

<span data-ttu-id="e2847-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e2847-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2847-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2847-118">Remarks</span></span>

<span data-ttu-id="e2847-119">Le applicazioni meno recenti (che hanno negoziato TAPI versione 1,3) ricevono un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE \_ reinit, per cui è necessario arrestare l'uso dell'API e chiamare di nuovo [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) per ottenere il nuovo numero di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e2847-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="e2847-120">Diversamente dalle versioni precedenti di TAPI, tuttavia, questa versione non richiede l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. la reinizializzazione può avvenire immediatamente quando viene creato un nuovo dispositivo. l'arresto completo è ancora necessario quando un provider di servizi viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e2847-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="e2847-121">Le applicazioni che supportano TAPI 1,4 o versione successiva vengono inviate un messaggio di **\_ creazione riga** .</span><span class="sxs-lookup"><span data-stu-id="e2847-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="e2847-122">In questo modo vengono segnalati l'esistenza del nuovo dispositivo e il nuovo identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2847-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="e2847-123">L'applicazione può quindi scegliere se provare a usare il nuovo dispositivo per lo svago.</span><span class="sxs-lookup"><span data-stu-id="e2847-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="e2847-124">Questo messaggio viene inviato a tutte le applicazioni che supportano questa o le versioni successive dell'API che hanno chiamato [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), inclusi quelli che non hanno dispositivi linea aperti al momento.</span><span class="sxs-lookup"><span data-stu-id="e2847-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2847-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2847-125">Requirements</span></span>



| <span data-ttu-id="e2847-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2847-126">Requirement</span></span> | <span data-ttu-id="e2847-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e2847-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e2847-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e2847-128">TAPI version</span></span><br/> | <span data-ttu-id="e2847-129">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e2847-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e2847-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2847-130">Header</span></span><br/>       | <dl> <span data-ttu-id="e2847-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2847-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2847-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2847-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2847-133">**LINEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2847-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="e2847-134">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="e2847-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="e2847-135">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e2847-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




