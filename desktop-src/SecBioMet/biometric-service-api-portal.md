---
title: Windows Biometric Framework
description: È possibile usare l'API Windows Biometric Framework per creare applicazioni client che acquisiscono, salvano e confrontano in modo sicuro le informazioni biometriche dell'utente finale.
ms.assetid: d9ac9ec1-bb34-402d-a590-73d5070b97ba
keywords:
- API Windows Biometric Framework API Windows Biometric Framework
- API Windows Biometric Framework API di Windows Biometric Framework, home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4341f09f3141e1be77bcdf0987ee1273ffddcf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713441"
---
# <a name="windows-biometric-framework"></a><span data-ttu-id="65c57-105">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="65c57-105">Windows Biometric Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="65c57-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="65c57-106">Purpose</span></span>

<span data-ttu-id="65c57-107">È possibile usare l'API Windows Biometric Framework per creare applicazioni client che acquisiscono, salvano e confrontano in modo sicuro le informazioni biometriche dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="65c57-107">You can use the Windows Biometric Framework API to create client applications that securely capture, save, and compare end-user biometric information.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="65c57-108">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="65c57-108">Developer audience</span></span>

<span data-ttu-id="65c57-109">Gli sviluppatori che usano questa API dovrebbero avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="65c57-109">Developers who use this API should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="65c57-110">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="65c57-110">Run-time requirements</span></span>

<span data-ttu-id="65c57-111">L'API Windows Biometric Framework è supportata a partire da Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65c57-111">The Windows Biometric Framework API is supported beginning with Windows Server 2008 R2 and Windows 7.</span></span> <span data-ttu-id="65c57-112">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="65c57-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65c57-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="65c57-113">In this section</span></span>



| <span data-ttu-id="65c57-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="65c57-114">Topic</span></span>                                                                                       | <span data-ttu-id="65c57-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65c57-115">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65c57-116">Panoramica di Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="65c57-116">Biometric Framework overview</span></span>](biometric-framework-overview.md)<br/>                 | <span data-ttu-id="65c57-117">Viene descritto il supporto nativo per la biometria in Windows.</span><span class="sxs-lookup"><span data-stu-id="65c57-117">Describes the native support for biometrics in Windows.</span></span><br/>                                                                                       |
| [<span data-ttu-id="65c57-118">Creazione di applicazioni client</span><span class="sxs-lookup"><span data-stu-id="65c57-118">Creating client applications</span></span>](creating-client-applications.md)<br/>                 | <span data-ttu-id="65c57-119">È possibile usare l'API client per acquisire e usare le informazioni biometriche nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="65c57-119">You can use the client API to capture and use biometric information in your applications.</span></span><br/>                                                     |
| [<span data-ttu-id="65c57-120">Creazione di plug-in di adapter</span><span class="sxs-lookup"><span data-stu-id="65c57-120">Creating Adapter Plug-ins</span></span>](creating-adapter-plug-ins.md)<br/>                       | <span data-ttu-id="65c57-121">È possibile creare schede del motore, adattatori di sensori e adattatori di archiviazione usando gli argomenti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="65c57-121">You can create engine adapters, sensor adapters, and storage adapters using the topics in this section.</span></span><br/>                                       |
| [<span data-ttu-id="65c57-122">Creazione di un pool di sensori privato</span><span class="sxs-lookup"><span data-stu-id="65c57-122">Creating a Private Sensor Pool</span></span>](creating-a-private-sensor-pool.md)<br/>             | <span data-ttu-id="65c57-123">Esistono due tipi di pool di sensori: privato e di sistema.</span><span class="sxs-lookup"><span data-stu-id="65c57-123">There are two types of sensor pools: private and system.</span></span> <span data-ttu-id="65c57-124">In questa sezione vengono descritte le singole procedure e viene illustrato come creare un pool di sensori privati.</span><span class="sxs-lookup"><span data-stu-id="65c57-124">This section describes each and explains how to create a private sensor pool.</span></span> <br/>       |
| [<span data-ttu-id="65c57-125">Informazioni di riferimento sull'API Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="65c57-125">Windows Biometric Framework API Reference</span></span>](biometric-service-api-reference.md)<br/> | <span data-ttu-id="65c57-126">Descrizioni dettagliate di funzioni, strutture e altri elementi di programmazione che possono essere usati per creare applicazioni client e plug-in.</span><span class="sxs-lookup"><span data-stu-id="65c57-126">Detailed descriptions of functions, structures, and other programming elements that can be used to create a client applications and plug-ins.</span></span><br/> |



 

 

 





