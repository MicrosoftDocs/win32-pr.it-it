---
title: Codici di errore del dispositivo
description: I Metodi InvokeAction e QueryStateVariable restituiscono valori HRESULT che potrebbero indicare un errore del dispositivo, ovvero un errore ricevuto da un dispositivo certificato UPnP.
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474542"
---
# <a name="device-error-codes"></a><span data-ttu-id="10907-103">Codici di errore del dispositivo</span><span class="sxs-lookup"><span data-stu-id="10907-103">Device Error Codes</span></span>

<span data-ttu-id="10907-104">I metodi [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) restituiscono valori **HRESULT** che potrebbero indicare un errore del dispositivo, ovvero un errore ricevuto da un dispositivo certificato UPnP.</span><span class="sxs-lookup"><span data-stu-id="10907-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="10907-105">Se viene ricevuto un errore da un dispositivo, il metodo ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) o [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) restituisce un valore **HRESULT** basato sul codice di errore del dispositivo, come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="10907-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="10907-106">Poiché una conversione viene applicata al codice di errore del dispositivo per produrre un valore **HRESULT** , non è possibile leggere il codice di errore del dispositivo direttamente dal valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10907-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="10907-107">Conversione di un codice di errore del dispositivo in un HRESULT</span><span class="sxs-lookup"><span data-stu-id="10907-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="10907-108">Sono presenti codici di errore del dispositivo standard e non standard.</span><span class="sxs-lookup"><span data-stu-id="10907-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="10907-109">I codici standard hanno lo stesso significato in tutti i dispositivi certificati UPnP e hanno valori minori di 600.</span><span class="sxs-lookup"><span data-stu-id="10907-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="10907-110">I codici non standard sono specifici del fornitore e hanno valori compresi tra 600 e 899.</span><span class="sxs-lookup"><span data-stu-id="10907-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="10907-111">Indica se il codice di errore del dispositivo è standard determina il modo in cui viene generato il valore **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="10907-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="10907-112">Viene eseguito il mapping di un codice di errore standard del dispositivo a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10907-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="10907-113">Un codice di errore non standard del dispositivo è incorporato nel valore **HRESULT** applicando una formula.</span><span class="sxs-lookup"><span data-stu-id="10907-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="10907-114">Entrambe queste procedure possono essere invertite per determinare il codice di errore del dispositivo da un particolare valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10907-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="10907-115">Derivazione di un codice di errore del dispositivo da un valore HRESULT</span><span class="sxs-lookup"><span data-stu-id="10907-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="10907-116">Se il valore **HRESULT** è maggiore o uguale a **UPnP e \_ \_ Action \_ specific \_ base** (0x80040300) e minore o uguale a UPnP e **\_ \_ Action \_ specific \_ Max** (0x8004042B), il codice di errore del dispositivo non è conforme allo standard, utilizzare la formula nella sezione seguente per determinare il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="10907-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="10907-117">In caso contrario, il codice di errore del dispositivo è standard: usare la tabella nella sezione mapping per i codici di errore del dispositivo standard, che fornisce il mapping tra il valore **HRESULT** e il codice di errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10907-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="10907-118">Per una descrizione di testo dell'errore dopo una chiamata a [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), impostare il parametro *pvarRetVal* su una matrice vuota.</span><span class="sxs-lookup"><span data-stu-id="10907-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="10907-119">Al ritorno, questo parametro conterrà una descrizione di testo dell'errore, se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="10907-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="10907-120">Formula per i codici di errore del dispositivo non standard</span><span class="sxs-lookup"><span data-stu-id="10907-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="10907-121">Utilizzare la formula seguente se **l' \_ azione UPnP e la \_ \_ \_ base specifica dell'azione** ≤ **HRESULT** ≤ valore **\_ \_ \_ \_ massimo specifico per l'azione UPnP e**.</span><span class="sxs-lookup"><span data-stu-id="10907-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="10907-122">Codice di errore del dispositivo= (  -  **\_ \_ \_ \_ base specifica dell'azione E dell'azione** HRESULT) + **\_ \_ \_ base specifica dell'azione di errore**</span><span class="sxs-lookup"><span data-stu-id="10907-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="10907-123">Sostituendo i valori numerici effettivi, l'equazione è: codice errore dispositivo = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="10907-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="10907-124">Mapping per i codici di errore standard del dispositivo</span><span class="sxs-lookup"><span data-stu-id="10907-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="10907-125">Usare il mapping seguente se si  <  **specifica \_ una \_ \_ \_ base specifica dell'azione HRESULT UPnP E**.</span><span class="sxs-lookup"><span data-stu-id="10907-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="10907-126">Valore HRESULT</span><span class="sxs-lookup"><span data-stu-id="10907-126">HRESULT value</span></span>                    | <span data-ttu-id="10907-127">Codice di errore del dispositivo</span><span class="sxs-lookup"><span data-stu-id="10907-127">Device Error Code</span></span>                | <span data-ttu-id="10907-128">Valore effettivo</span><span class="sxs-lookup"><span data-stu-id="10907-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="10907-129">\_azione UPnP E \_ non valida \_</span><span class="sxs-lookup"><span data-stu-id="10907-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="10907-130">ERRORE \_ azione non valida \_</span><span class="sxs-lookup"><span data-stu-id="10907-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="10907-131">401</span><span class="sxs-lookup"><span data-stu-id="10907-131">401</span></span>          |
| <span data-ttu-id="10907-132">\_argomenti UPnP E \_ non validi \_</span><span class="sxs-lookup"><span data-stu-id="10907-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="10907-133">ERRORE \_ arg non valido \_</span><span class="sxs-lookup"><span data-stu-id="10907-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="10907-134">402</span><span class="sxs-lookup"><span data-stu-id="10907-134">402</span></span>          |
| <span data-ttu-id="10907-135">UPNP \_ E \_ non \_ \_ sincronizzati</span><span class="sxs-lookup"><span data-stu-id="10907-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="10907-136">ERRORE \_ \_ numero di sequenza non valido \_</span><span class="sxs-lookup"><span data-stu-id="10907-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="10907-137">403</span><span class="sxs-lookup"><span data-stu-id="10907-137">403</span></span>          |
| <span data-ttu-id="10907-138">UPNP \_ E \_ variabile non valida \_</span><span class="sxs-lookup"><span data-stu-id="10907-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="10907-139">variabile di errore \_ non valida \_</span><span class="sxs-lookup"><span data-stu-id="10907-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="10907-140">404</span><span class="sxs-lookup"><span data-stu-id="10907-140">404</span></span>          |
| <span data-ttu-id="10907-141">\_richiesta di azione UPnP E \_ \_ \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="10907-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="10907-142">\_ \_ errore interno del dispositivo di errore \_</span><span class="sxs-lookup"><span data-stu-id="10907-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="10907-143">501</span><span class="sxs-lookup"><span data-stu-id="10907-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="10907-144">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="10907-144">More Information</span></span>

<span data-ttu-id="10907-145">I codici di errore del dispositivo sono specificati nella [versione 1,0 dell'architettura del dispositivo UPnP](https://openconnectivity.org/resources/documents.asp).</span><span class="sxs-lookup"><span data-stu-id="10907-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="10907-146">Le costanti indicate in questo argomento sono definite nei file UPnP. h e UPnP. idl.</span><span class="sxs-lookup"><span data-stu-id="10907-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




