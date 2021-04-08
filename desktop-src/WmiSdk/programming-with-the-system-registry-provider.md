---
description: Negli argomenti seguenti viene descritto il modo in cui le applicazioni possono utilizzare il provider del registro di sistema per fornire i dati per le classi create.
ms.assetid: 84604fbc-50b2-410d-84bf-4a408be26ee2
ms.tgt_platform: multiple
title: Programmazione con il provider del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c31563a7a4ef22f1de7c4c697b201ff998a73c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879961"
---
# <a name="programming-with-the-system-registry-provider"></a><span data-ttu-id="37d0c-103">Programmazione con il provider del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="37d0c-103">Programming with the System Registry Provider</span></span>

<span data-ttu-id="37d0c-104">Negli argomenti seguenti viene descritto il modo in cui le applicazioni possono utilizzare il provider del registro di sistema per fornire i dati per le classi create.</span><span class="sxs-lookup"><span data-stu-id="37d0c-104">The following topics describe how applications can use the System Registry Provider to provide data for classes that you create.</span></span>



| <span data-ttu-id="37d0c-105">Argomento</span><span class="sxs-lookup"><span data-stu-id="37d0c-105">Topic</span></span>                                                                                                                      | <span data-ttu-id="37d0c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37d0c-106">Description</span></span>                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37d0c-107">Definizione delle classi per il provider del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="37d0c-107">Defining Classes for the System Registry Provider</span></span>](defining-classes-for-the-system-registry-provider.md)                 | <span data-ttu-id="37d0c-108">Per accedere al registro di sistema, è necessario creare classi Windows che archiviano le informazioni del registro di sistema nel repository Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="37d0c-108">To access the system registry, you must create Windows classes that store registry information in the Windows Management Instrumentation (WMI) repository.</span></span>                                                                     |
| [<span data-ttu-id="37d0c-109">Uso del provider del registro di sistema come provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="37d0c-109">Using the System Registry Provider as a Property Provider</span></span>](using-the-system-registry-provider-as-a-property-provider.md) | <span data-ttu-id="37d0c-110">Il provider del registro di sistema richiede l'utilizzo di diversi qualificatori per visualizzare le proprietà del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d0c-110">The System Registry Provider requires that you use several qualifiers to view registry properties.</span></span>                                                                                                                             |
| [<span data-ttu-id="37d0c-111">Descrizione di una risorsa per il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="37d0c-111">Describing a Resource for the Registry</span></span>](describing-a-resource-for-the-registry.md)                                       | <span data-ttu-id="37d0c-112">È possibile accedere ai dati nel registro di sistema che descrive una risorsa di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d0c-112">You can access data in the registry that describes a system resource.</span></span> <span data-ttu-id="37d0c-113">Per modificare le informazioni, il provider del registro di sistema richiede una sintassi specifica.</span><span class="sxs-lookup"><span data-stu-id="37d0c-113">To modify the information, the System Registry Provider requires a specific syntax.</span></span>                                                                      |
| [<span data-ttu-id="37d0c-114">Accesso a un valore del registro di sistema senza nome</span><span class="sxs-lookup"><span data-stu-id="37d0c-114">Accessing an Unnamed Registry Value</span></span>](accessing-an-unnamed-registry-value.md)                                             | <span data-ttu-id="37d0c-115">Per accedere alla maggior parte dei valori del registro di sistema, creare una classe per ricevere i valori in WMI oppure è possibile esaminare specifiche proprietà del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d0c-115">To access most registry values, create a class to receive the values in WMI, or you can examine specific registry properties.</span></span> <span data-ttu-id="37d0c-116">Tuttavia, il provider del registro di sistema richiede una sintassi speciale per visualizzare i valori del registro di sistema senza nome.</span><span class="sxs-lookup"><span data-stu-id="37d0c-116">However, the System Registry Provider requires a special syntax to view unnamed registry values.</span></span> |



 

 

 



