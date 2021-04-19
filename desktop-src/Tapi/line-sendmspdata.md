---
description: Il messaggio TSPI LINE \_ SENDMSPDATA viene inviato quando il provider di servizi di telefonia (TSP) vuole passare informazioni al provider di servizi multimediali (msp).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Messaggio LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326624"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="430ee-103">\_Messaggio linea SENDMSPDATA</span><span class="sxs-lookup"><span data-stu-id="430ee-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="430ee-104">Il messaggio TSPI **line \_ SENDMSPDATA** viene inviato quando il provider di servizi di telefonia (TSP) vuole passare informazioni al provider di servizi multimediali (msp).</span><span class="sxs-lookup"><span data-stu-id="430ee-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="430ee-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="430ee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430ee-106">*htLine*</span><span class="sxs-lookup"><span data-stu-id="430ee-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-107">Handle TAPI per la riga.</span><span class="sxs-lookup"><span data-stu-id="430ee-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="430ee-108">*htCall*</span><span class="sxs-lookup"><span data-stu-id="430ee-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-109">Handle TAPI per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="430ee-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="430ee-110">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="430ee-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-111">RIGA del valore \_ SENDMSPDATA.</span><span class="sxs-lookup"><span data-stu-id="430ee-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="430ee-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="430ee-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-113">Identifica il MSP che deve ricevere il messaggio.</span><span class="sxs-lookup"><span data-stu-id="430ee-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="430ee-114">Se è 0, il messaggio verrà inviato a tutti MSPs.</span><span class="sxs-lookup"><span data-stu-id="430ee-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="430ee-115">Si tratta dell'handle passato alla funzione [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .</span><span class="sxs-lookup"><span data-stu-id="430ee-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="430ee-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="430ee-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-117">Buffer da passare al MSP.</span><span class="sxs-lookup"><span data-stu-id="430ee-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="430ee-118">Il buffer non è interpretato da TAPI.</span><span class="sxs-lookup"><span data-stu-id="430ee-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="430ee-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="430ee-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="430ee-120">Dimensione, in byte, del buffer in *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="430ee-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="430ee-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="430ee-121">Remarks</span></span>

<span data-ttu-id="430ee-122">Per il corretto funzionamento di questo messaggio, il provider di servizi deve negoziare una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="430ee-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="430ee-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="430ee-123">Requirements</span></span>



| <span data-ttu-id="430ee-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="430ee-124">Requirement</span></span> | <span data-ttu-id="430ee-125">Valore</span><span class="sxs-lookup"><span data-stu-id="430ee-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="430ee-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="430ee-126">TAPI version</span></span><br/> | <span data-ttu-id="430ee-127">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="430ee-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="430ee-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="430ee-128">Header</span></span><br/>       | <dl> <span data-ttu-id="430ee-129"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="430ee-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430ee-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="430ee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430ee-131">Informazioni sul provider di servizi multimediali (MSP)</span><span class="sxs-lookup"><span data-stu-id="430ee-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="430ee-132">**\_LINEMSPIDENTIFY TSPI**</span><span class="sxs-lookup"><span data-stu-id="430ee-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="430ee-133">**\_LINECREATEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="430ee-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="430ee-134">**\_LINECLOSEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="430ee-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="430ee-135">**\_LINERECIEVEMSPDATA TSPI**</span><span class="sxs-lookup"><span data-stu-id="430ee-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="430ee-136">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="430ee-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

