---
title: Creazione di un pool di sensori privato
description: Come usare l'API Windows Biometric Framework per creare un pool di sensori privati.
ms.assetid: 79944E30-A3D4-411D-A551-3B309DEA6FEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eda88f8a9bd0befcbf5527e52d572ec7ca55ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396578"
---
# <a name="creating-a-private-sensor-pool"></a><span data-ttu-id="fba2d-103">Creazione di un pool di sensori privato</span><span class="sxs-lookup"><span data-stu-id="fba2d-103">Creating a Private Sensor Pool</span></span>

<span data-ttu-id="fba2d-104">Un pool di sensori privati è una raccolta di unità biometriche riservate per l'uso esclusivo da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="fba2d-104">A private sensor pool is a collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="fba2d-105">I pool privati supportano i metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="fba2d-105">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span>

<span data-ttu-id="fba2d-106">Negli argomenti seguenti sono contenuti esempi di codice che illustrano come creare un pool di sensori privati.</span><span class="sxs-lookup"><span data-stu-id="fba2d-106">The following topics contain code examples that show how to create a private sensor pool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fba2d-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="fba2d-107">In this section</span></span>



| <span data-ttu-id="fba2d-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="fba2d-108">Topic</span></span>                                                                         | <span data-ttu-id="fba2d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fba2d-109">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fba2d-110">Pool di sensori</span><span class="sxs-lookup"><span data-stu-id="fba2d-110">Sensor Pools</span></span>](sensor-pools.md)<br/>                                   | <span data-ttu-id="fba2d-111">Vengono descritti tre possibili pool di sensori: sistema, privato e non assegnato.</span><span class="sxs-lookup"><span data-stu-id="fba2d-111">Describes three possible sensor pools: system, private, and unassigned.</span></span><br/>                   |
| [<span data-ttu-id="fba2d-112">Impostazione del pool privato</span><span class="sxs-lookup"><span data-stu-id="fba2d-112">Private Pool Setup</span></span>](private-pool-setup.md)<br/>                       | <span data-ttu-id="fba2d-113">Contiene il progetto della console di installazione.</span><span class="sxs-lookup"><span data-stu-id="fba2d-113">Contains the setup console project.</span></span><br/>                                                       |
| [<span data-ttu-id="fba2d-114">Identità del pool privato</span><span class="sxs-lookup"><span data-stu-id="fba2d-114">Private Pool Identity</span></span>](private-pool-identity.md)<br/>                 | <span data-ttu-id="fba2d-115">Contiene il progetto della console di identificazione.</span><span class="sxs-lookup"><span data-stu-id="fba2d-115">Contains the identification console project.</span></span><br/>                                              |
| [<span data-ttu-id="fba2d-116">Registrazione del pool privato</span><span class="sxs-lookup"><span data-stu-id="fba2d-116">Private Pool Enrollment</span></span>](private-pool-enrollment.md)<br/>             | <span data-ttu-id="fba2d-117">Contiene il progetto della console di registrazione.</span><span class="sxs-lookup"><span data-stu-id="fba2d-117">Contains the enrollment console project.</span></span><br/>                                                  |
| [<span data-ttu-id="fba2d-118">Funzioni di supporto del pool privato</span><span class="sxs-lookup"><span data-stu-id="fba2d-118">Private Pool Helper Functions</span></span>](private-pool-helper-functions.md)<br/> | <span data-ttu-id="fba2d-119">Contiene le funzioni di supporto per i progetti console di installazione, identificazione e registrazione.</span><span class="sxs-lookup"><span data-stu-id="fba2d-119">Contains helper functions for the setup, identification, and enrollment console projects.</span></span><br/> |
| [<span data-ttu-id="fba2d-120">Creazione di applicazioni client</span><span class="sxs-lookup"><span data-stu-id="fba2d-120">Create client applications</span></span>](creating-client-applications.md)<br/>     | <span data-ttu-id="fba2d-121">Come usare l'API Windows Biometric Framework per creare applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="fba2d-121">How to use the Windows Biometric Framework API to create client applications.</span></span><br/>             |



 

 

 





