---
description: Usare le tecnologie di crittografia per la crittografia a chiave pubblica, gli algoritmi di crittografia, la crittografia RSA e i certificati digitali.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306447"
---
# <a name="cryptography"></a><span data-ttu-id="3a38a-103">Crittografia</span><span class="sxs-lookup"><span data-stu-id="3a38a-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="3a38a-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="3a38a-104">Purpose</span></span>

<span data-ttu-id="3a38a-105">La crittografia prevede l'uso di codici per la conversione dei dati in modo che solo un destinatario specifico possa leggerlo, usando una chiave.</span><span class="sxs-lookup"><span data-stu-id="3a38a-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="3a38a-106">Le tecnologie di crittografia Microsoft includono CryptoAPI, provider del servizio di crittografia (CSP), strumenti CryptoAPI, capicol, WinTrust, emissione e gestione dei certificati e sviluppo di infrastrutture a chiave pubblica personalizzabili.</span><span class="sxs-lookup"><span data-stu-id="3a38a-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="3a38a-107">Vengono descritti anche la registrazione di certificati e smart card, la gestione dei certificati e lo sviluppo di moduli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3a38a-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3a38a-108">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3a38a-108">Developer audience</span></span>

<span data-ttu-id="3a38a-109">CryptoAPI è progettato per l'uso da parte di sviluppatori di applicazioni basate su Windows che consentono agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet.</span><span class="sxs-lookup"><span data-stu-id="3a38a-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="3a38a-110">Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione Windows.</span><span class="sxs-lookup"><span data-stu-id="3a38a-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="3a38a-111">Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia o gli argomenti relativi alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3a38a-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="3a38a-112">CAPICOM è un componente solo a 32 bit che deve essere utilizzato dagli sviluppatori che creano applicazioni utilizzando il linguaggio di programmazione di Visual Basic Scripting Edition (VBScript) o il linguaggio di programmazione C++.</span><span class="sxs-lookup"><span data-stu-id="3a38a-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="3a38a-113">CAPICOM è disponibile per l'uso nei sistemi operativi specificati in Run-Time requirements.</span><span class="sxs-lookup"><span data-stu-id="3a38a-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="3a38a-114">Per lo sviluppo futuro, è consigliabile usare la .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3a38a-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="3a38a-115">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).</span><span class="sxs-lookup"><span data-stu-id="3a38a-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3a38a-116">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="3a38a-116">Run-time requirements</span></span>

<span data-ttu-id="3a38a-117">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="3a38a-118">CAPICOM 2.1.0.2 è supportato nei sistemi operativi e nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a38a-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="3a38a-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a38a-119">Windows Server 2003</span></span>
-   <span data-ttu-id="3a38a-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a38a-120">Windows XP</span></span>

<span data-ttu-id="3a38a-121">CAPICOM è disponibile come file ridistribuibile che può essere scaricato da [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span><span class="sxs-lookup"><span data-stu-id="3a38a-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="3a38a-122">Servizi certificati richiede le seguenti versioni di questi sistemi operativi:</span><span class="sxs-lookup"><span data-stu-id="3a38a-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="3a38a-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a38a-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="3a38a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a38a-124">Windows Server 2008</span></span>
-   <span data-ttu-id="3a38a-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a38a-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a38a-126">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3a38a-126">In this section</span></span>



| <span data-ttu-id="3a38a-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="3a38a-127">Topic</span></span>                                                           | <span data-ttu-id="3a38a-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a38a-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a38a-129">Informazioni sulla crittografia</span><span class="sxs-lookup"><span data-stu-id="3a38a-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="3a38a-130">Concetti chiave di crittografia e una panoramica di alto livello delle tecnologie di crittografia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a38a-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="3a38a-131">Uso della crittografia</span><span class="sxs-lookup"><span data-stu-id="3a38a-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="3a38a-132">Processi di crittografia, procedure ed esempi estesi di programmi C e Visual Basic con funzioni CryptoAPI e oggetti CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="3a38a-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="3a38a-133">Informazioni di riferimento sulla crittografia</span><span class="sxs-lookup"><span data-stu-id="3a38a-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="3a38a-134">Descrizioni dettagliate delle funzioni di crittografia Microsoft, delle interfacce, degli oggetti, delle strutture e di altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="3a38a-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="3a38a-135">Include le descrizioni di riferimento dell'API per l'uso di certificati digitali.</span><span class="sxs-lookup"><span data-stu-id="3a38a-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




