---
title: Pubblicazione con la registrazione di Windows Sockets & risoluzione
description: I servizi Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Active Directory per la registrazione e la risoluzione di Windows Sockets, pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2019
ms.locfileid: "104472091"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="00b84-104">Pubblicazione con la registrazione di Windows Sockets & risoluzione</span><span class="sxs-lookup"><span data-stu-id="00b84-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="00b84-105">I servizi Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR.</span><span class="sxs-lookup"><span data-stu-id="00b84-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="00b84-106">La pubblicazione RnR viene eseguita in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="00b84-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="00b84-107">Il primo passaggio installa una classe del servizio che associa un GUID a un nome per il servizio.</span><span class="sxs-lookup"><span data-stu-id="00b84-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="00b84-108">La classe del servizio può mantenere i dati di configurazione specifici del servizio.</span><span class="sxs-lookup"><span data-stu-id="00b84-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="00b84-109">I servizi possono quindi essere pubblicati come istanze della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="00b84-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="00b84-110">Al momento della pubblicazione, i client possono eseguire query nel servizio directory per le istanze di una determinata classe usando le API RnR e selezionare un'istanza a cui eseguire l'associazione.</span><span class="sxs-lookup"><span data-stu-id="00b84-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="00b84-111">Quando una classe non è più necessaria, può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="00b84-111">When a class is no longer required, it can be removed.</span></span>

 

 




