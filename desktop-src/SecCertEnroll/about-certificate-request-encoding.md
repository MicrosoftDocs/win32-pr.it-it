---
description: In un'infrastruttura a chiave pubblica Microsoft, le richieste di certificati vengono inviate da computer client alle autorità di certificazione (CAs) come stringa binaria che contiene una sequenza di strutture di dati codificate.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codifica della richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756545"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="7ff9e-103">Codifica della richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="7ff9e-103">Certificate Request Encoding</span></span>

<span data-ttu-id="7ff9e-104">In un'infrastruttura a chiave pubblica Microsoft, le richieste di certificati vengono inviate da computer client alle autorità di certificazione (CAs) come stringa binaria che contiene una sequenza di strutture di dati codificate.</span><span class="sxs-lookup"><span data-stu-id="7ff9e-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="7ff9e-105">L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per descrivere e codificare queste strutture.</span><span class="sxs-lookup"><span data-stu-id="7ff9e-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="7ff9e-106">Ai fini di questa documentazione, ASN. 1 può essere concettualmente suddiviso nelle regole di sintassi (ISO 8824) che descrivono le strutture dei dati e le regole di codifica (ISO 8825) che specificano la modalità di codifica dei dati per la trasmissione di rete.</span><span class="sxs-lookup"><span data-stu-id="7ff9e-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="7ff9e-107">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="7ff9e-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7ff9e-108">Introduzione alla sintassi e alla codifica ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7ff9e-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="7ff9e-109">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7ff9e-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="7ff9e-110">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="7ff9e-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="7ff9e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ff9e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ff9e-112">Informazioni sull'API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="7ff9e-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



