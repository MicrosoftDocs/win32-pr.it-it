---
description: Il sistema carica un provider di tempo in base alle informazioni di configurazione archiviate nel registro di sistema.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrazione di un provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882350"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="2a374-103">Registrazione di un provider Time</span><span class="sxs-lookup"><span data-stu-id="2a374-103">Registering a Time Provider</span></span>

<span data-ttu-id="2a374-104">Il sistema carica un provider di tempo in base alle informazioni di configurazione archiviate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2a374-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="2a374-105">Ogni provider di servizi temporali deve creare la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="2a374-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="2a374-106">**HKEY \_ \_Computer locale \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *providerName*</span><span class="sxs-lookup"><span data-stu-id="2a374-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="2a374-107">Nella tabella seguente vengono descritti i valori che devono esistere nella chiave di ogni provider.</span><span class="sxs-lookup"><span data-stu-id="2a374-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="2a374-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2a374-108">Value</span></span>             | <span data-ttu-id="2a374-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a374-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a374-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="2a374-110">**DllName**</span></span>       | <span data-ttu-id="2a374-111">Nome della DLL che contiene il provider.</span><span class="sxs-lookup"><span data-stu-id="2a374-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="2a374-112">Questo valore è di tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="2a374-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="2a374-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="2a374-113">**Enabled**</span></span>       | <span data-ttu-id="2a374-114">Indica se il provider deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="2a374-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="2a374-115">Se questo valore è 1, il provider viene avviato.</span><span class="sxs-lookup"><span data-stu-id="2a374-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="2a374-116">In caso contrario, il provider non viene avviato.</span><span class="sxs-lookup"><span data-stu-id="2a374-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="2a374-117">Questo valore è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2a374-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="2a374-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="2a374-118">**InputProvider**</span></span> | <span data-ttu-id="2a374-119">Indica se il provider è un provider di input o un provider di output.</span><span class="sxs-lookup"><span data-stu-id="2a374-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="2a374-120">Se questo valore è 1, il provider è un provider di input.</span><span class="sxs-lookup"><span data-stu-id="2a374-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="2a374-121">In caso contrario, il provider è un provider di output.</span><span class="sxs-lookup"><span data-stu-id="2a374-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="2a374-122">Questo valore è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2a374-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="2a374-123">Gestione provider di servizi temporali enumera le chiavi sotto la chiave **TimeProviders** e avvia ogni provider abilitato.</span><span class="sxs-lookup"><span data-stu-id="2a374-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="2a374-124">I provider vengono avviati all'avvio del sistema e ogni volta che vengono apportate modifiche ai parametri.</span><span class="sxs-lookup"><span data-stu-id="2a374-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="2a374-125">Ogni provider di servizi temporali può inoltre archiviare informazioni di configurazione specifiche dell'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2a374-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



