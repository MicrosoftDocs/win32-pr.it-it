---
description: TAPI invia il \_ messaggio DEVSPECIFIC del telefono a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si verificano sul telefono. Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Messaggio di PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324128"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="f2faa-104">\_Messaggio DEVSPECIFIC telefono</span><span class="sxs-lookup"><span data-stu-id="f2faa-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="f2faa-105">TAPI invia il **messaggio \_ DEVSPECIFIC del telefono** a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si verificano sul telefono.</span><span class="sxs-lookup"><span data-stu-id="f2faa-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="f2faa-106">Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="f2faa-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f2faa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2faa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2faa-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="f2faa-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="f2faa-109">Handle per il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f2faa-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f2faa-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f2faa-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f2faa-111">Istanza di callback dell'applicazione fornita all'apertura del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f2faa-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f2faa-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f2faa-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f2faa-113">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2faa-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="f2faa-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f2faa-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f2faa-115">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2faa-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="f2faa-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f2faa-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f2faa-117">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2faa-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2faa-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2faa-118">Return value</span></span>

<span data-ttu-id="f2faa-119">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f2faa-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2faa-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2faa-120">Requirements</span></span>



| <span data-ttu-id="f2faa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2faa-121">Requirement</span></span> | <span data-ttu-id="f2faa-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f2faa-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2faa-123">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f2faa-123">TAPI version</span></span><br/> | <span data-ttu-id="f2faa-124">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f2faa-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f2faa-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2faa-125">Header</span></span><br/>       | <dl> <span data-ttu-id="f2faa-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2faa-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




