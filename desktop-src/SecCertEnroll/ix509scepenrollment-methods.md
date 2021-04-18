---
description: L'interfaccia IX509SCEPEnrollment espone i metodi seguenti.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Metodi IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314714"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="21e2e-103">Metodi IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="21e2e-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="21e2e-104">L'interfaccia [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="21e2e-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="21e2e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="21e2e-105">In this section</span></span>



| <span data-ttu-id="21e2e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="21e2e-106">Topic</span></span>                                                                                                              | <span data-ttu-id="21e2e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21e2e-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21e2e-108">**Metodo CreateRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="21e2e-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="21e2e-109">Creare un messaggio di richiesta PKCS10 con una password di verifica.</span><span class="sxs-lookup"><span data-stu-id="21e2e-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="21e2e-110">Il messaggio di richiesta si trova in una busta di PKCS7 crittografata con il certificato di crittografia del server SCEP e firmata dal certificato di firma del server.</span><span class="sxs-lookup"><span data-stu-id="21e2e-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="21e2e-111">**Metodo CreateRetrieveCertificateMessage**</span><span class="sxs-lookup"><span data-stu-id="21e2e-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="21e2e-112">Recuperare un certificato emesso in precedenza.</span><span class="sxs-lookup"><span data-stu-id="21e2e-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="21e2e-113">**Metodo CreateRetrievePendingMessage**</span><span class="sxs-lookup"><span data-stu-id="21e2e-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="21e2e-114">Creare un messaggio per il polling del certificato (registrazione manuale).</span><span class="sxs-lookup"><span data-stu-id="21e2e-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="21e2e-115">**Metodo DeleteRequest**</span><span class="sxs-lookup"><span data-stu-id="21e2e-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="21e2e-116">Eliminare tutti i certificati o le chiavi create per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="21e2e-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="21e2e-117">**Initialize (metodo)**</span><span class="sxs-lookup"><span data-stu-id="21e2e-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="21e2e-118">Inizializzare l'istanza di in preparazione per una nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="21e2e-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="21e2e-119">**Metodo InitializeForPending**</span><span class="sxs-lookup"><span data-stu-id="21e2e-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="21e2e-120">Inizializzare l'istanza di per preparare la generazione di un messaggio per recuperare un certificato emesso o per installare una risposta per una richiesta precedente da parte dell'emittente.</span><span class="sxs-lookup"><span data-stu-id="21e2e-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="21e2e-121">**Metodo ProcessResponseMessage**</span><span class="sxs-lookup"><span data-stu-id="21e2e-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="21e2e-122">Elaborare un messaggio di risposta e restituire la disposizione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="21e2e-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




