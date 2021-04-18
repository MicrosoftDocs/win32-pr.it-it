---
description: L'interfaccia IX509SCEPEnrollment espone le proprietà seguenti.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Proprietà di IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314713"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="c5326-103">Proprietà di IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="c5326-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="c5326-104">L'interfaccia [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5326-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5326-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c5326-105">In this section</span></span>



| <span data-ttu-id="c5326-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="c5326-106">Topic</span></span>                                                                                              | <span data-ttu-id="c5326-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5326-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5326-108">**Proprietà certificato**</span><span class="sxs-lookup"><span data-stu-id="c5326-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="c5326-109">Ottiene il certificato per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c5326-110">**Proprietà CertificateFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="c5326-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="c5326-111">Ottiene o imposta il nome descrittivo per il certificato.</span><span class="sxs-lookup"><span data-stu-id="c5326-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c5326-112">**Proprietà FailInfo**</span><span class="sxs-lookup"><span data-stu-id="c5326-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="c5326-113">Ottiene informazioni quando il metodo [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) rileva un ambiente non riuscito.</span><span class="sxs-lookup"><span data-stu-id="c5326-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="c5326-114">**Proprietà OldCertificate**</span><span class="sxs-lookup"><span data-stu-id="c5326-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="c5326-115">Ottiene o imposta un certificato obsoleto che deve essere sostituito da una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="c5326-116">**Proprietà della richiesta**</span><span class="sxs-lookup"><span data-stu-id="c5326-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="c5326-117">Ottiene la richiesta PKCS10 interna.</span><span class="sxs-lookup"><span data-stu-id="c5326-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="c5326-118">**Proprietà ServerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c5326-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="c5326-119">Imposta gli algoritmi di crittografia e hash preferiti per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="c5326-120">**Proprietà SignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="c5326-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="c5326-121">Ottiene o imposta il certificato del firmatario per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c5326-122">**Proprietà invisibile all'utente**</span><span class="sxs-lookup"><span data-stu-id="c5326-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="c5326-123">Ottiene o imposta un valore che indica se consentire l'interfaccia utente durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c5326-124">**Status (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="c5326-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="c5326-125">Ottiene lo stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c5326-126">**Proprietà ID transazione**</span><span class="sxs-lookup"><span data-stu-id="c5326-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="c5326-127">Ottiene o imposta l'ID della transazione per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5326-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




