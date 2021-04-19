---
description: Il messaggio del pulsante del telefono TAPI \_ viene inviato per notificare all'applicazione che il pulsante di monitoraggio è abilitato se è stato rilevato un pulsante premuto sul telefono locale.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Messaggio di PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329211"
---
# <a name="phone_button-message"></a><span data-ttu-id="60310-103">\_Messaggio del pulsante telefonico</span><span class="sxs-lookup"><span data-stu-id="60310-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="60310-104">Il messaggio **del \_ pulsante del telefono** TAPI viene inviato per notificare all'applicazione che il pulsante di monitoraggio è abilitato se è stato rilevato un pulsante premuto sul telefono locale.</span><span class="sxs-lookup"><span data-stu-id="60310-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="60310-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="60310-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60310-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="60310-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="60310-107">Handle per il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="60310-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="60310-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="60310-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="60310-109">Istanza di callback dell'applicazione fornita all'apertura del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="60310-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="60310-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="60310-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="60310-111">Identificatore pulsante/Lamp del pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="60310-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="60310-112">Si noti che gli identificatori di pulsante da zero a 11 sono sempre i pulsanti del TASTIERino, con ' 0' come identificatore del pulsante zero,' 1' è l'identificatore del pulsante 1 (e così via tramite l'identificatore del pulsante 9) e con '' è l'identificatore del \* pulsante 10 è \# ' è l'identificatore del pulsante 11.</span><span class="sxs-lookup"><span data-stu-id="60310-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="60310-113">Altre informazioni su un identificatore di pulsante sono disponibili con [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span><span class="sxs-lookup"><span data-stu-id="60310-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="60310-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="60310-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="60310-115">Modalità del pulsante.</span><span class="sxs-lookup"><span data-stu-id="60310-115">The button mode of the button.</span></span> <span data-ttu-id="60310-116">Questo parametro usa una delle [**\_ costanti PHONEBUTTONMODE**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="60310-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="60310-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="60310-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="60310-118">Specifica se si tratta di un evento di un pulsante o di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="60310-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="60310-119">Questo parametro usa una delle [**\_ costanti PHONEBUTTONSTATE**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="60310-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60310-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60310-120">Return value</span></span>

<span data-ttu-id="60310-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="60310-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60310-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="60310-122">Remarks</span></span>

<span data-ttu-id="60310-123">Un messaggio di un **\_ pulsante telefonico** viene inviato ogni volta che viene modificato lo stato di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="60310-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="60310-124">A un'applicazione viene garantito che per ogni evento button down viene inviato un evento Button up corrispondente.</span><span class="sxs-lookup"><span data-stu-id="60310-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="60310-125">Un provider di servizi che non è in grado di rilevare il pulsante effettivo attivo è necessario per generare il messaggio di riattivazione del pulsante subito dopo il messaggio premuto per ogni pressione del pulsante.</span><span class="sxs-lookup"><span data-stu-id="60310-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="60310-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60310-126">Requirements</span></span>



| <span data-ttu-id="60310-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="60310-127">Requirement</span></span> | <span data-ttu-id="60310-128">Valore</span><span class="sxs-lookup"><span data-stu-id="60310-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="60310-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="60310-129">TAPI version</span></span><br/> | <span data-ttu-id="60310-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="60310-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="60310-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60310-131">Header</span></span><br/>       | <dl> <span data-ttu-id="60310-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="60310-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60310-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60310-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60310-134">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="60310-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="60310-135">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="60310-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




