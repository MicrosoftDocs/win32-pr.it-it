---
description: Il messaggio di creazione del telefono TAPI \_ viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Messaggio di PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325278"
---
# <a name="phone_create-message"></a><span data-ttu-id="9eef5-103">Telefono \_ Creazione messaggio</span><span class="sxs-lookup"><span data-stu-id="9eef5-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="9eef5-104">Il messaggio **di \_ creazione del telefono** TAPI viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="9eef5-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9eef5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eef5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eef5-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="9eef5-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="9eef5-107">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9eef5-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9eef5-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="9eef5-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9eef5-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9eef5-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9eef5-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9eef5-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9eef5-111">*HDeviceID* del dispositivo appena creato.</span><span class="sxs-lookup"><span data-stu-id="9eef5-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="9eef5-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9eef5-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9eef5-113">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9eef5-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9eef5-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9eef5-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9eef5-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9eef5-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eef5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eef5-116">Return value</span></span>

<span data-ttu-id="9eef5-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9eef5-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eef5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eef5-118">Remarks</span></span>

<span data-ttu-id="9eef5-119">Le applicazioni che hanno negoziato l'API versione 1,3 ricevono un messaggio di [**\_ stato del telefono**](phone-state.md) che specifica PHONESTATE \_ reinit, per cui è necessario arrestare l'uso dell'API e chiamare di nuovo [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) per ottenere il nuovo numero di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9eef5-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="9eef5-120">Tuttavia, la versione 1,4 e successive di TAPI non richiedono l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. la reinizializzazione può avvenire immediatamente quando viene creato un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9eef5-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="9eef5-121">Le applicazioni che supportano TAPI 1,4 o versioni successive vengono inviate un messaggio di **\_ creazione telefono** .</span><span class="sxs-lookup"><span data-stu-id="9eef5-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="9eef5-122">In questo modo vengono segnalati l'esistenza del nuovo dispositivo e il nuovo identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9eef5-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="9eef5-123">L'applicazione può quindi scegliere se provare a usare il nuovo dispositivo per lo svago.</span><span class="sxs-lookup"><span data-stu-id="9eef5-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eef5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eef5-124">Requirements</span></span>



| <span data-ttu-id="9eef5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eef5-125">Requirement</span></span> | <span data-ttu-id="9eef5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9eef5-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9eef5-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9eef5-127">TAPI version</span></span><br/> | <span data-ttu-id="9eef5-128">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9eef5-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9eef5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eef5-129">Header</span></span><br/>       | <dl> <span data-ttu-id="9eef5-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eef5-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eef5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eef5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eef5-132">**\_stato telefono**</span><span class="sxs-lookup"><span data-stu-id="9eef5-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="9eef5-133">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="9eef5-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="9eef5-134">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="9eef5-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




