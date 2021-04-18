---
description: Il messaggio della linea TAPI \_ DEVSPECIFICEX viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Messaggio di LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330465"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="6eb28-104">\_Messaggio linea DEVSPECIFICEX</span><span class="sxs-lookup"><span data-stu-id="6eb28-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="6eb28-105">Il messaggio della **linea TAPI \_ DEVSPECIFICEX** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata.</span><span class="sxs-lookup"><span data-stu-id="6eb28-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="6eb28-106">Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6eb28-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6eb28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eb28-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6eb28-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6eb28-109">Handle per un dispositivo o una chiamata a linee.</span><span class="sxs-lookup"><span data-stu-id="6eb28-109">A handle to either a line device or call.</span></span> <span data-ttu-id="6eb28-110">Questo parametro è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6eb28-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6eb28-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6eb28-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="6eb28-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6eb28-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6eb28-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6eb28-114">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6eb28-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6eb28-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6eb28-116">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6eb28-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6eb28-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6eb28-118">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eb28-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6eb28-119">Return value</span></span>

<span data-ttu-id="6eb28-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6eb28-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eb28-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6eb28-121">Remarks</span></span>

<span data-ttu-id="6eb28-122">Il messaggio di **riga \_ DEVSPECIFICEX** viene utilizzato da un provider di servizi insieme alla funzione [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="6eb28-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="6eb28-123">Il suo significato è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eb28-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb28-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6eb28-124">Requirements</span></span>



| <span data-ttu-id="6eb28-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb28-125">Requirement</span></span> | <span data-ttu-id="6eb28-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6eb28-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6eb28-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6eb28-127">TAPI version</span></span><br/> | <span data-ttu-id="6eb28-128">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6eb28-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6eb28-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6eb28-129">Header</span></span><br/>       | <dl> <span data-ttu-id="6eb28-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb28-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




