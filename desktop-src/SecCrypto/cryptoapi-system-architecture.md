---
description: Viene illustrata l'architettura del sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Architettura del sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343141"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="e2e64-103">Architettura del sistema CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="e2e64-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="e2e64-104">L'architettura di sistema CryptoAPI è costituita da cinque aree funzionali principali:</span><span class="sxs-lookup"><span data-stu-id="e2e64-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="e2e64-105">Funzioni di crittografia di base</span><span class="sxs-lookup"><span data-stu-id="e2e64-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="e2e64-106">Funzioni codifica/decodifica certificati</span><span class="sxs-lookup"><span data-stu-id="e2e64-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="e2e64-107">Funzioni dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="e2e64-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="e2e64-108">Funzioni di messaggio semplificate</span><span class="sxs-lookup"><span data-stu-id="e2e64-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="e2e64-109">Funzioni di messaggio di basso livello</span><span class="sxs-lookup"><span data-stu-id="e2e64-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="e2e64-110">Funzioni di crittografia di base</span><span class="sxs-lookup"><span data-stu-id="e2e64-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="e2e64-111">*Funzioni di contesto* utilizzate per la connessione a un CSP.</span><span class="sxs-lookup"><span data-stu-id="e2e64-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="e2e64-112">Queste funzioni consentono alle applicazioni di scegliere un CSP specifico in base al nome o di scegliere un CSP specifico che può fornire una classe necessaria di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e2e64-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="e2e64-113">[*Funzioni di generazione*](../secgloss/k-gly.md) delle chiavi utilizzate per generare e archiviare le [*chiavi crittografiche*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="e2e64-114">Il supporto completo è incluso per modificare le [*modalità di concatenamento*](../secgloss/c-gly.md), i [*vettori di inizializzazione*](../secgloss/i-gly.md)e altre funzionalità di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e2e64-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="e2e64-115">Per altre informazioni, vedere [generazione di chiavi e funzioni di Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="e2e64-116">*Funzioni di scambio* delle chiavi usate per scambiare o trasmettere chiavi.</span><span class="sxs-lookup"><span data-stu-id="e2e64-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="e2e64-117">Per altre informazioni, vedere [archiviazione delle chiavi crittografiche ed Exchange](cryptographic-key-storage-and-exchange.md) e [funzioni di generazione e scambio di chiavi](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="e2e64-118">Funzioni codifica/decodifica certificati</span><span class="sxs-lookup"><span data-stu-id="e2e64-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="e2e64-119">Funzioni usate per crittografare o decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="e2e64-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="e2e64-120">È incluso anche il supporto per l' [*hashing*](../secgloss/h-gly.md) dei dati.</span><span class="sxs-lookup"><span data-stu-id="e2e64-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="e2e64-121">Per altre informazioni, vedere [funzioni di crittografia](cryptography-functions.md) e decrittografia dei dati e [crittografia e decrittografia dei dati](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="e2e64-122">Funzioni dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="e2e64-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="e2e64-123">Funzioni utilizzate per gestire le raccolte di certificati digitali.</span><span class="sxs-lookup"><span data-stu-id="e2e64-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="e2e64-124">Per ulteriori informazioni, vedere [certificati digitali](digital-certificates.md) e [funzioni di archivio certificati](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="e2e64-125">Funzioni di messaggio semplificate</span><span class="sxs-lookup"><span data-stu-id="e2e64-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="e2e64-126">Funzioni utilizzate per crittografare e decrittografare i messaggi e i dati.</span><span class="sxs-lookup"><span data-stu-id="e2e64-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="e2e64-127">Funzioni utilizzate per firmare messaggi e dati.</span><span class="sxs-lookup"><span data-stu-id="e2e64-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="e2e64-128">Funzioni utilizzate per verificare l'autenticità delle firme nei messaggi ricevuti e nei dati correlati.</span><span class="sxs-lookup"><span data-stu-id="e2e64-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="e2e64-129">Per ulteriori informazioni, vedere [messaggi semplificati](simplified-messages.md) e [funzioni di messaggio semplificate](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="e2e64-130">Funzioni di messaggio di basso livello</span><span class="sxs-lookup"><span data-stu-id="e2e64-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="e2e64-131">Funzioni utilizzate per eseguire tutte le attività eseguite dalle funzioni di messaggio semplificate.</span><span class="sxs-lookup"><span data-stu-id="e2e64-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="e2e64-132">Le funzioni di messaggio di basso livello offrono maggiore flessibilità rispetto alle funzioni di messaggio semplificate, ma richiedono più chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="e2e64-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="e2e64-133">Per ulteriori informazioni, vedere [messaggi di basso livello](low-level-messages.md) e [funzioni di messaggio di basso livello](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![architettura CryptoAPI](images/cryparch.png)

<span data-ttu-id="e2e64-135">Ogni area funzionale ha una parola chiave nel nome della funzione che ne indica l'area funzionale.</span><span class="sxs-lookup"><span data-stu-id="e2e64-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="e2e64-136">Area funzionale</span><span class="sxs-lookup"><span data-stu-id="e2e64-136">Functional area</span></span>              | <span data-ttu-id="e2e64-137">Convenzione nome funzione</span><span class="sxs-lookup"><span data-stu-id="e2e64-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="e2e64-138">Funzioni di crittografia di base</span><span class="sxs-lookup"><span data-stu-id="e2e64-138">Base cryptographic functions</span></span> | <span data-ttu-id="e2e64-139">Cripta</span><span class="sxs-lookup"><span data-stu-id="e2e64-139">Crypt</span></span>                    |
| <span data-ttu-id="e2e64-140">Funzioni di codifica/decodifica</span><span class="sxs-lookup"><span data-stu-id="e2e64-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="e2e64-141">Cripta</span><span class="sxs-lookup"><span data-stu-id="e2e64-141">Crypt</span></span>                    |
| <span data-ttu-id="e2e64-142">Funzioni dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="e2e64-142">Certificate store functions</span></span>  | <span data-ttu-id="e2e64-143">Archivio</span><span class="sxs-lookup"><span data-stu-id="e2e64-143">Store</span></span>                    |
| <span data-ttu-id="e2e64-144">Funzioni di messaggio semplificate</span><span class="sxs-lookup"><span data-stu-id="e2e64-144">Simplified message functions</span></span> | <span data-ttu-id="e2e64-145">Message</span><span class="sxs-lookup"><span data-stu-id="e2e64-145">Message</span></span>                  |
| <span data-ttu-id="e2e64-146">Funzioni di messaggio di basso livello</span><span class="sxs-lookup"><span data-stu-id="e2e64-146">Low-level message functions</span></span>  | <span data-ttu-id="e2e64-147">Msg</span><span class="sxs-lookup"><span data-stu-id="e2e64-147">Msg</span></span>                      |



 

<span data-ttu-id="e2e64-148">Le applicazioni utilizzano funzioni in tutte queste aree.</span><span class="sxs-lookup"><span data-stu-id="e2e64-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="e2e64-149">Queste funzioni, combinate, costituiscono CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="e2e64-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="e2e64-150">Le [*funzioni di crittografia di base*](../secgloss/b-gly.md) utilizzano i CSP per gli algoritmi di crittografia necessari e per la generazione e l'archiviazione sicura delle [chiavi crittografiche](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="e2e64-151">Vengono utilizzati due tipi diversi di chiavi crittografiche: [*chiavi di sessione*](../secgloss/s-gly.md), utilizzate per una singola crittografia/decrittografia e coppie di [*chiavi pubbliche/private*](../secgloss/p-gly.md), che vengono utilizzate in modo più permanente.</span><span class="sxs-lookup"><span data-stu-id="e2e64-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="e2e64-152">Sebbene un'applicazione possa comunicare direttamente con una delle cinque aree funzionali, non può comunicare direttamente con un CSP.</span><span class="sxs-lookup"><span data-stu-id="e2e64-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="e2e64-153">Tutte le comunicazioni da applicazione a CSP avvengono tramite le [*funzioni di crittografia di base*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2e64-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="e2e64-154">Le funzioni di crittografia di base dispongono di un parametro che specifica il CSP da usare.</span><span class="sxs-lookup"><span data-stu-id="e2e64-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="e2e64-155">Questo parametro può essere impostato su **null** per selezionare un CSP predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2e64-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
