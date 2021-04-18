---
description: Il messaggio della linea TAPI \_ DEVSPECIFICFEATURE viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Messaggio di LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333652"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="1d396-104">\_Messaggio linea DEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="1d396-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="1d396-105">Il messaggio della **linea TAPI \_ DEVSPECIFICFEATURE** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata.</span><span class="sxs-lookup"><span data-stu-id="1d396-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="1d396-106">Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d396-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1d396-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d396-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d396-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="1d396-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="1d396-109">Handle per un dispositivo o una chiamata a linee.</span><span class="sxs-lookup"><span data-stu-id="1d396-109">A handle to either a line device or call.</span></span> <span data-ttu-id="1d396-110">Si tratta di un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="1d396-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d396-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="1d396-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1d396-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="1d396-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="1d396-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1d396-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1d396-114">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d396-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d396-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1d396-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1d396-116">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d396-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d396-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1d396-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1d396-118">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d396-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d396-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d396-119">Return value</span></span>

<span data-ttu-id="1d396-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1d396-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d396-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d396-121">Remarks</span></span>

<span data-ttu-id="1d396-122">Il messaggio di **riga \_ DEVSPECIFICFEATURE** viene utilizzato da un provider di servizi insieme alla funzione [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="1d396-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="1d396-123">Il suo significato è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d396-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d396-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d396-124">Requirements</span></span>



| <span data-ttu-id="1d396-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d396-125">Requirement</span></span> | <span data-ttu-id="1d396-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1d396-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d396-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="1d396-127">TAPI version</span></span><br/> | <span data-ttu-id="1d396-128">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1d396-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1d396-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d396-129">Header</span></span><br/>       | <dl> <span data-ttu-id="1d396-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d396-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




