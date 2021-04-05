---
description: Usare i comandi MakeCert per creare certificati di test usando le opzioni disponibili con Internet Explorer versione 4,0 o successiva.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso di MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753447"
---
# <a name="using-makecert"></a><span data-ttu-id="933ae-103">Uso di MakeCert</span><span class="sxs-lookup"><span data-stu-id="933ae-103">Using MakeCert</span></span>

<span data-ttu-id="933ae-104">Negli esempi seguenti vengono utilizzati i comandi [Makecert](makecert.md) per creare certificati di test utilizzando le opzioni disponibili con Internet Explorer versione 4,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="933ae-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="933ae-105">Creare un certificato emesso dalla radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="933ae-106">Salvare il certificato in un file.</span><span class="sxs-lookup"><span data-stu-id="933ae-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="933ae-107">**Makecert** *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="933ae-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="933ae-108">Creare un certificato emesso dalla radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="933ae-109">Salvarlo in un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="933ae-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="933ae-110">**Makecert-SS** *MyNewStore*</span><span class="sxs-lookup"><span data-stu-id="933ae-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="933ae-111">Creare un certificato emesso dalla radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="933ae-112">Creare un contenitore di chiavi e salvare il certificato in un archivio e in un file.</span><span class="sxs-lookup"><span data-stu-id="933ae-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="933ae-113">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="933ae-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="933ae-114">Creare un certificato emesso dalla radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="933ae-115">Creare un file di chiave privata e salvare il certificato in un archivio e in un file.</span><span class="sxs-lookup"><span data-stu-id="933ae-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="933ae-116">**Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="933ae-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="933ae-117">Creare un certificato emesso dalla radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="933ae-118">Creare un contenitore di chiavi, salvare il certificato in un archivio e in un file e rendere esportabile la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="933ae-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="933ae-119">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**</span><span class="sxs-lookup"><span data-stu-id="933ae-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="933ae-120">Creare un certificato usando la radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="933ae-121">Salvare il certificato in un archivio.</span><span class="sxs-lookup"><span data-stu-id="933ae-121">Save the certificate to a store.</span></span> <span data-ttu-id="933ae-122">Quindi, creare un altro certificato emesso dal certificato appena creato.</span><span class="sxs-lookup"><span data-stu-id="933ae-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="933ae-123">Salvare il secondo certificato in un altro archivio.</span><span class="sxs-lookup"><span data-stu-id="933ae-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="933ae-124">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="933ae-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="933ae-125">Creare un certificato usando la radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="933ae-126">Salvare il certificato nell'archivio personale.</span><span class="sxs-lookup"><span data-stu-id="933ae-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="933ae-127">Quindi creare un altro certificato usando il certificato appena creato.</span><span class="sxs-lookup"><span data-stu-id="933ae-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="933ae-128">Se è presente più di un certificato nell'archivio MY, il certificato deve essere identificato con il nome comune.</span><span class="sxs-lookup"><span data-stu-id="933ae-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="933ae-129">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My Makecert-is My-in "XXZZYY"-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="933ae-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="933ae-130">Creare un certificato usando la radice di test predefinita.</span><span class="sxs-lookup"><span data-stu-id="933ae-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="933ae-131">Salvare il certificato nell'archivio personale e in un file.</span><span class="sxs-lookup"><span data-stu-id="933ae-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="933ae-132">Quindi creare un altro certificato usando il certificato *MyNew* appena creato.</span><span class="sxs-lookup"><span data-stu-id="933ae-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="933ae-133">Se è presente più di un certificato nell'archivio MY, identificare in modo univoco il primo certificato usando il nome del file del certificato.</span><span class="sxs-lookup"><span data-stu-id="933ae-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="933ae-134">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is my-IC** *MyNew. cer* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="933ae-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



