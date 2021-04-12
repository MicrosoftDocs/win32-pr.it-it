---
description: Esempio di certificato. Creare applicazioni per la certificazione API, installare il certificato SSL, il certificato del server, creare il certificato su supporti, ad esempio Internet o una rete Intranet, che non sono intrinsecamente protetti.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API di registrazione certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526335"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="bd54c-104">API di registrazione certificato</span><span class="sxs-lookup"><span data-stu-id="bd54c-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="bd54c-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="bd54c-105">Purpose</span></span>

<span data-ttu-id="bd54c-106">L'API di registrazione certificati può essere usata per creare un'applicazione client per richiedere un certificato e installare una risposta del certificato.</span><span class="sxs-lookup"><span data-stu-id="bd54c-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="bd54c-107">Questa API è implementata in CertEnroll.dll a partire da Windows Vista; sostituisce Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="bd54c-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bd54c-108">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="bd54c-108">Developer audience</span></span>

<span data-ttu-id="bd54c-109">L'API di registrazione certificati è destinata agli sviluppatori di applicazioni che consentiranno agli utenti di creare, richiedere e recuperare i certificati su supporti, ad esempio Internet o una rete Intranet, che non sono intrinsecamente protetti.</span><span class="sxs-lookup"><span data-stu-id="bd54c-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="bd54c-110">Gli sviluppatori dovrebbero avere familiarità con i linguaggi di programmazione C e C++, il Component Object Model (COM) e l'ambiente di programmazione basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="bd54c-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="bd54c-111">Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia e l'infrastruttura a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="bd54c-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bd54c-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="bd54c-112">Run-time requirements</span></span>

<span data-ttu-id="bd54c-113">L'API di registrazione certificati è supportata a partire da Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bd54c-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="bd54c-114">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="bd54c-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd54c-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bd54c-115">In this section</span></span>



| <span data-ttu-id="bd54c-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="bd54c-116">Topic</span></span>                                                                                       | <span data-ttu-id="bd54c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd54c-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd54c-118">Informazioni sull'API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="bd54c-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="bd54c-119">Vengono illustrati i concetti chiave relativi alle richieste di certificato.</span><span class="sxs-lookup"><span data-stu-id="bd54c-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="bd54c-120">Uso dell'API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="bd54c-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="bd54c-121">Come usare l'API di registrazione certificati per estendere le funzionalità di Active Directory Servizi certificati.</span><span class="sxs-lookup"><span data-stu-id="bd54c-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="bd54c-122">Informazioni di riferimento sulle API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="bd54c-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="bd54c-123">Descrizioni dettagliate di interfacce, enumerazioni e altri elementi di programmazione che possono essere utilizzati per registrare un utente o un computer in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="bd54c-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




