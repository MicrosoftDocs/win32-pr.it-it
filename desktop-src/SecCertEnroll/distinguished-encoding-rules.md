---
description: Abstract Syntax Notation One (ASN. 1) definisce i set di regole seguenti che determinano il modo in cui le strutture dei dati inviate tra i computer vengono codificate e decodificate.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527001"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="7aa2f-103">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="7aa2f-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="7aa2f-104">Abstract Syntax Notation One (ASN. 1) definisce i set di regole seguenti che determinano il modo in cui le strutture dei dati inviate tra i computer vengono codificate e decodificate.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="7aa2f-105">Regole di codifica di base (BER)</span><span class="sxs-lookup"><span data-stu-id="7aa2f-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="7aa2f-106">Regole di codifica canoniche (CER)</span><span class="sxs-lookup"><span data-stu-id="7aa2f-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="7aa2f-107">Distinguished Encoding Rules (DER)</span><span class="sxs-lookup"><span data-stu-id="7aa2f-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="7aa2f-108">Regole di codifica compresse (PER)</span><span class="sxs-lookup"><span data-stu-id="7aa2f-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="7aa2f-109">Il set di regole originale è stato definito dalla specifica BER.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="7aa2f-110">CER e DER sono stati sviluppati in seguito come subset specializzati di BER.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="7aa2f-111">PER è stato sviluppato in risposta a critiche sulla quantità di larghezza di banda necessaria per trasmettere i dati utilizzando BER o le relative varianti.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="7aa2f-112">PER fornisce un notevole risparmio.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-112">PER provides a significant savings.</span></span>

<span data-ttu-id="7aa2f-113">DER è stato creato per soddisfare i requisiti della specifica X. 509 per il trasferimento sicuro dei dati.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="7aa2f-114">L'API di registrazione certificati usa esclusivamente DER.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="7aa2f-115">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="7aa2f-116">Sintassi di trasferimento DER</span><span class="sxs-lookup"><span data-stu-id="7aa2f-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="7aa2f-117">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7aa2f-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="7aa2f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7aa2f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aa2f-119">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7aa2f-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="7aa2f-120">Codifica della richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="7aa2f-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="7aa2f-121">Introduzione alla sintassi e alla codifica ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7aa2f-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



