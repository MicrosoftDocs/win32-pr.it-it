---
description: Questa sezione include scenari che usano le procedure di CAPICOM.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Uso di CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527624"
---
# <a name="using-capicom"></a><span data-ttu-id="0557a-103">Uso di CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0557a-103">Using CAPICOM</span></span>

<span data-ttu-id="0557a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0557a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0557a-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0557a-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="0557a-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="0557a-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="0557a-107">Questa sezione include scenari che usano le procedure di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="0557a-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="0557a-108">La creazione di [*firme digitali*](../secgloss/d-gly.md) e la disattivazione di messaggi con CAPICOM viene eseguita usando la crittografia a chiave pubblica (PKI) e può essere eseguita solo se il firmatario o l'utente che decrittografa un messaggio in busta ha accesso a un certificato con una chiave privata disponibile associata.</span><span class="sxs-lookup"><span data-stu-id="0557a-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="0557a-109">Per decrittografare un messaggio in busta digitale, un certificato con accesso alla chiave privata deve trovarsi nell'archivio personale.</span><span class="sxs-lookup"><span data-stu-id="0557a-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="0557a-110">Negli scenari basati su attività sono stati illustrati gli esempi e le discussioni è stata suddivisa nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0557a-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="0557a-111">Alternative all'uso di CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0557a-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="0557a-112">Preparazione all'uso di CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0557a-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="0557a-113">Crittografia e decrittografia di dati</span><span class="sxs-lookup"><span data-stu-id="0557a-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="0557a-114">Firma dei dati e verifica delle firme digitali</span><span class="sxs-lookup"><span data-stu-id="0557a-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="0557a-115">Uso degli archivi certificati</span><span class="sxs-lookup"><span data-stu-id="0557a-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="0557a-116">Creazione e ricezione di messaggi di dati in busta digitale</span><span class="sxs-lookup"><span data-stu-id="0557a-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
