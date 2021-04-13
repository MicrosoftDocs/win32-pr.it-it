---
title: Componente provider di esempio ADSI
description: Active Directory i writer del provider di interfacce del servizio troveranno questa sezione di particolare interesse, perché descrive in modo dettagliato il componente del provider di esempio ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328452"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="706e6-103">Componente provider di esempio ADSI</span><span class="sxs-lookup"><span data-stu-id="706e6-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="706e6-104">Active Directory i writer del provider di interfacce del servizio troveranno questa sezione di particolare interesse, perché descrive in modo dettagliato il componente del provider di esempio ADSI.</span><span class="sxs-lookup"><span data-stu-id="706e6-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="706e6-105">I writer del provider ADSI possono installare il provider di esempio e utilizzare il Framework di codice come base per creare la propria implementazione.</span><span class="sxs-lookup"><span data-stu-id="706e6-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="706e6-106">Vengono trattati i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="706e6-106">The following topics are discussed:</span></span>

<span data-ttu-id="706e6-107">L' [installazione del componente provider di esempio](installing-the-example-provider-component.md) descrive come installare il provider di esempio ADSI e la relativa directory fittizia.</span><span class="sxs-lookup"><span data-stu-id="706e6-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="706e6-108">Questa sezione include un elenco delle impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="706e6-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="706e6-109">La [definizione della directory](directory-definition.md) descrive le voci di directory definite dal componente provider di esempio.</span><span class="sxs-lookup"><span data-stu-id="706e6-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="706e6-110">[Gestione schema](schema-management.md) descrive il modo in cui ogni elemento nel servizio directory del componente provider di esempio può essere rappresentato da un tipo specifico di oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="706e6-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="706e6-111">Il [binding a un oggetto Active Directory](binding-to-an-active-directory-object.md) descrive in che modo, data una stringa ADsPath, il componente provider di esempio identifica tale elemento, crea il tipo appropriato di Active Directory oggetto e recupera il tipo di puntatore di interfaccia richiesto su tale oggetto per passare di nuovo al software client ADS.</span><span class="sxs-lookup"><span data-stu-id="706e6-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="706e6-112">[Oggetti enumeratore](enumerator-objects.md) elenca i tipi specifici di enumerazioni fornite dal componente provider di esempio e il codice sorgente in cui è possibile trovare le implementazioni.</span><span class="sxs-lookup"><span data-stu-id="706e6-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="706e6-113">[Cenni preliminari sul codice](code-overview.md) fornisce una descrizione a livello di attività di ogni parte del componente provider di esempio.</span><span class="sxs-lookup"><span data-stu-id="706e6-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="706e6-114">[Dettagli codice](code-details.md) elenca i moduli software e il relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="706e6-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 




