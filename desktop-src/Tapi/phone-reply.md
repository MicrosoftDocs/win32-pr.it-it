---
description: Il messaggio di risposta del telefono TAPI \_ viene inviato a un'applicazione per segnalare i risultati della chiamata di funzione completata in modo asincrono.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Messaggio di PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324126"
---
# <a name="phone_reply-message"></a><span data-ttu-id="0b0c9-103">\_Messaggio di risposta telefono</span><span class="sxs-lookup"><span data-stu-id="0b0c9-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="0b0c9-104">Il messaggio **di \_ risposta del telefono** TAPI viene inviato a un'applicazione per segnalare i risultati della chiamata di funzione completata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="0b0c9-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b0c9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b0c9-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="0b0c9-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="0b0c9-107">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="0b0c9-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="0b0c9-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0b0c9-109">Restituisce l'istanza di callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="0b0c9-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0b0c9-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b0c9-111">Identificatore della richiesta per cui si tratta della risposta.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="0b0c9-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0b0c9-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b0c9-113">Indicazione di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-113">The success or error indication.</span></span> <span data-ttu-id="0b0c9-114">L'applicazione deve eseguire il cast di questo parametro in un valore LONG.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="0b0c9-115">Zero indica esito positivo; un numero negativo indica un errore.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="0b0c9-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0b0c9-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0b0c9-117">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b0c9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b0c9-118">Return value</span></span>

<span data-ttu-id="0b0c9-119">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b0c9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b0c9-120">Remarks</span></span>

<span data-ttu-id="0b0c9-121">Le funzioni che operano in modo asincrono restituiscono un valore di identificatore di richiesta positivo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="0b0c9-122">Questo identificatore di richiesta viene restituito con il messaggio di risposta per identificare la richiesta completata.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="0b0c9-123">L'altro parametro per il messaggio di **\_ risposta telefonica** contiene l'indicazione di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="0b0c9-124">Gli errori possibili sono gli stessi di quelli definiti dalla funzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="0b0c9-125">Questo messaggio non può essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0b0c9-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0c9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b0c9-126">Requirements</span></span>



| <span data-ttu-id="0b0c9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0c9-127">Requirement</span></span> | <span data-ttu-id="0b0c9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0b0c9-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0b0c9-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0b0c9-129">TAPI version</span></span><br/> | <span data-ttu-id="0b0c9-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0b0c9-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0b0c9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b0c9-131">Header</span></span><br/>       | <dl> <span data-ttu-id="0b0c9-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0c9-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




