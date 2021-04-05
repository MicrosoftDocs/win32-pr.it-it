---
description: L'operazione di prelievo consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo. L'applicazione identifica la destinazione del pickup e restituisce un identificatore di sessione per la chiamata selezionata.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Prelievo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758336"
---
# <a name="pickup"></a><span data-ttu-id="aa714-104">Prelievo</span><span class="sxs-lookup"><span data-stu-id="aa714-104">Pickup</span></span>

<span data-ttu-id="aa714-105">L'operazione di prelievo consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo.</span><span class="sxs-lookup"><span data-stu-id="aa714-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="aa714-106">L'applicazione identifica la destinazione del pickup e restituisce un identificatore di sessione per la chiamata selezionata.</span><span class="sxs-lookup"><span data-stu-id="aa714-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="aa714-107">Esistono diversi modi per identificare la destinazione della richiesta di prelievo.</span><span class="sxs-lookup"><span data-stu-id="aa714-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="aa714-108">In primo luogo, l'applicazione può specificare l'indirizzo della parte di avviso.</span><span class="sxs-lookup"><span data-stu-id="aa714-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="aa714-109">In secondo luogo, se non viene specificato alcun indirizzo e l'opzione lo consente, l'applicazione può prelevare qualsiasi sessione di avviso nel gruppo di prelievo.</span><span class="sxs-lookup"><span data-stu-id="aa714-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="aa714-110">In terzo luogo, alcuni commutatori consentono il ritiro di un avviso di sessione in un gruppo di prelievo diverso se viene specificato l'identificatore di gruppo.</span><span class="sxs-lookup"><span data-stu-id="aa714-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="aa714-111">Alcuni sistemi telefonici principali supportano un *trasferimento tramite* la funzionalità di attesa su un aspetto di chiamata Bridged-Exclusive.</span><span class="sxs-lookup"><span data-stu-id="aa714-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="aa714-112">In questo schema, un telefono specifico è proprietario di una chiamata esclusivamente quando la chiamata è attiva, ma quando la chiamata è in attesa, qualsiasi telefono con un aspetto della linea può prelevare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="aa714-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="aa714-113">**TAPI 2. x:** Un'applicazione può usare un'operazione di prelievo con un indirizzo di destinazione **null** a questo scopo, in modo analogo a come viene usata la funzione per prelevare una chiamata in attesa su una linea analoga.</span><span class="sxs-lookup"><span data-stu-id="aa714-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="aa714-114">LINEADDRFEATURE \_ PICKUPHELD indica l'esistenza della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aa714-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="aa714-115">Se LINEADDRCAPFLAGS \_ PICKUPCALLWAIT è **true**, è possibile prelevare una sessione per la quale l'utente ha rilevato in modo udibile il segnale in attesa di chiamata, ma per il quale il provider di servizi non è in grado di eseguire il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="aa714-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="aa714-116">Questo consente all'utente un meccanismo per "rispondere" a una chiamata in attesa anche se il provider di servizi non è stato in grado di rilevare il segnale in attesa di chiamata.</span><span class="sxs-lookup"><span data-stu-id="aa714-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="aa714-117">Sia l'indirizzo di destinazione che l'ID gruppo devono essere **null** per scegliere una chiamata in attesa.</span><span class="sxs-lookup"><span data-stu-id="aa714-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="aa714-118">Quando una sessione viene prelevata correttamente, l'applicazione riceve una notifica di modifica dello stato con il [motivo](reason-ovr.md) impostato su LINECALLREASON \_ pickup.</span><span class="sxs-lookup"><span data-stu-id="aa714-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="aa714-119">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="aa714-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="aa714-120">**TAPI 2. x:** Vedere [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="aa714-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="aa714-121">**TAPI 3. x:** Vedere [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="aa714-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
