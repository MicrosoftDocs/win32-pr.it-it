---
description: Informazioni su come creare un gestore delle proprietà che legge e scrive le proprietà in e da un flusso di file. Ogni gestore è associato a un determinato tipo di file.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementazione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481836"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="22c8d-104">Implementazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-104">Implementing Property Handlers</span></span>

<span data-ttu-id="22c8d-105">In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo di organizzazione di elementi come file, messaggi di posta elettronica o contatti.</span><span class="sxs-lookup"><span data-stu-id="22c8d-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="22c8d-106">Per abilitare un sistema in cui è possibile eseguire ricerche di elementi in base ai relativi metadati e in cui gli utenti possono leggere o scrivere i metadati, Windows Vista ha introdotto un nuovo sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="22c8d-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="22c8d-107">I metadati in questo sistema sono rappresentati da un set estendibile di proprietà.</span><span class="sxs-lookup"><span data-stu-id="22c8d-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="22c8d-108">In questo set di argomenti viene descritto come creare un gestore che legge e scrive le proprietà in e da un flusso di file.</span><span class="sxs-lookup"><span data-stu-id="22c8d-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="22c8d-109">Questi gestori sono denominati gestori di proprietà e ognuno è associato a un determinato tipo di file, identificato dall'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="22c8d-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="22c8d-110">Negli argomenti seguenti vengono illustrati i requisiti e le strategie necessari per definire le proprietà e i gestori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="22c8d-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="22c8d-111">Informazioni sui gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="22c8d-112">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="22c8d-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="22c8d-113">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="22c8d-114">Inizializzazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="22c8d-115">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="22c8d-116">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="22c8d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22c8d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c8d-118">Creazione di proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="22c8d-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="22c8d-119">Schema di descrizione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="22c8d-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
