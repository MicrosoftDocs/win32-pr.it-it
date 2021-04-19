---
description: Il messaggio ADDRESSSTATE della linea TAPI \_ viene inviato quando lo stato di un indirizzo viene modificato in una riga attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAddressStatus per determinare lo stato corrente dell'indirizzo.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Messaggio di LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326744"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="42659-104">\_Messaggio linea ADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="42659-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="42659-105">Il messaggio **\_ ADDRESSSTATE della linea** TAPI viene inviato quando lo stato di un indirizzo viene modificato in una riga attualmente aperta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42659-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="42659-106">L'applicazione può richiamare [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) per determinare lo stato corrente dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="42659-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="42659-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="42659-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42659-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="42659-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="42659-109">Handle per il dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="42659-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="42659-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="42659-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="42659-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="42659-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="42659-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="42659-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="42659-113">Identificatore dell'indirizzo che ha modificato lo stato.</span><span class="sxs-lookup"><span data-stu-id="42659-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="42659-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="42659-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="42659-115">Stato dell'indirizzo modificato.</span><span class="sxs-lookup"><span data-stu-id="42659-115">The address state that changed.</span></span> <span data-ttu-id="42659-116">Può essere una o più delle [**\_ costanti LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="42659-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="42659-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="42659-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="42659-118">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="42659-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42659-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42659-119">Return value</span></span>

<span data-ttu-id="42659-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="42659-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42659-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="42659-121">Remarks</span></span>

<span data-ttu-id="42659-122">Il messaggio di **riga \_ ADDRESSSTATE** viene inviato a qualsiasi applicazione che ha aperto il dispositivo a linee e che ha abilitato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="42659-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="42659-123">L'invio di questo messaggio per i vari elementi di stato può essere controllato e sottoposto a query usando [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) e [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="42659-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="42659-124">Per impostazione predefinita, la creazione di report sullo stato degli indirizzi è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="42659-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="42659-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42659-125">Requirements</span></span>



| <span data-ttu-id="42659-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42659-126">Requirement</span></span> | <span data-ttu-id="42659-127">Valore</span><span class="sxs-lookup"><span data-stu-id="42659-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="42659-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="42659-128">TAPI version</span></span><br/> | <span data-ttu-id="42659-129">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="42659-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="42659-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42659-130">Header</span></span><br/>       | <dl> <span data-ttu-id="42659-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="42659-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42659-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42659-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42659-133">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="42659-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="42659-134">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="42659-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="42659-135">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="42659-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="42659-136">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="42659-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="42659-137">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="42659-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




