---
description: Viene illustrato come Servizi certificati elabora le richieste di certificati.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Elaborazione delle richieste di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555696"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="6d275-103">Elaborazione delle richieste di certificati</span><span class="sxs-lookup"><span data-stu-id="6d275-103">Processing Certificate Requests</span></span>

<span data-ttu-id="6d275-104">Durante l'elaborazione di una [*richiesta di certificato*](../secgloss/c-gly.md), Servizi certificati esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d275-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="6d275-105">Richiedere la ricezione.</span><span class="sxs-lookup"><span data-stu-id="6d275-105">Request reception.</span></span>

    <span data-ttu-id="6d275-106">La [*richiesta di certificato*](../secgloss/c-gly.md) viene inviata dal client a un'applicazione intermedia, che la formatta in una \# richiesta di formato PKCS 10 e la invia al motore del server.</span><span class="sxs-lookup"><span data-stu-id="6d275-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="6d275-107">Richiedi l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="6d275-107">Request approval.</span></span>

    <span data-ttu-id="6d275-108">Il motore del server chiama il [modulo criteri](policy-modules.md), che esegue query sulle proprietà della richiesta, decide se la richiesta è autorizzata o meno e imposta le proprietà facoltative del certificato.</span><span class="sxs-lookup"><span data-stu-id="6d275-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="6d275-109">Formazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="6d275-109">Certificate formation.</span></span>

    <span data-ttu-id="6d275-110">Se la richiesta viene approvata, il motore del server accetta la richiesta e tutte le proprietà richieste dal modulo criteri e compila un certificato completo.</span><span class="sxs-lookup"><span data-stu-id="6d275-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="6d275-111">Pubblicazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="6d275-111">Certificate publication.</span></span>

    <span data-ttu-id="6d275-112">Il motore Server archivia il certificato completato nel database di Servizi certificati e notifica all'applicazione intermedia lo stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="6d275-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="6d275-113">Se il [modulo di uscita](exit-modules.md) è stato richiesto, il motore del server invierà una notifica di un evento di rilascio del certificato.</span><span class="sxs-lookup"><span data-stu-id="6d275-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="6d275-114">Ciò consente al modulo di uscita di eseguire ulteriori operazioni, ad esempio la pubblicazione del certificato in un repository di certificati esterno, ad esempio un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="6d275-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="6d275-115">Nel frattempo, l'intermediario ottiene il certificato pubblicato da Servizi certificati e lo passa nuovamente al client.</span><span class="sxs-lookup"><span data-stu-id="6d275-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="6d275-116">Nella figura seguente viene illustrato come una [*richiesta di certificato*](../secgloss/c-gly.md) viene elaborata da Servizi certificati.</span><span class="sxs-lookup"><span data-stu-id="6d275-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![elaborazione di una richiesta di certificato](images/certflow.png)

 

 
