---
description: In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo per organizzare elementi quali file, posta elettronica o contatti.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementazione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232521"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="5cffe-103">Implementazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-103">Implementing Property Handlers</span></span>

<span data-ttu-id="5cffe-104">In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo per organizzare elementi quali file, posta elettronica o contatti.</span><span class="sxs-lookup"><span data-stu-id="5cffe-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="5cffe-105">Per abilitare un sistema in cui è possibile eseguire la ricerca di elementi in base ai relativi metadati e dove gli utenti possono leggere o scrivere i metadati, Windows Vista ha introdotto un nuovo sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5cffe-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="5cffe-106">I metadati in questo sistema sono rappresentati da un set estendibile di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5cffe-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="5cffe-107">In questo set di argomenti viene descritto come creare un gestore che legge e scrive le proprietà in e da un flusso di file.</span><span class="sxs-lookup"><span data-stu-id="5cffe-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="5cffe-108">Questi gestori sono denominati gestori di proprietà e ognuno è associato a un determinato tipo di file, identificato dall'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="5cffe-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="5cffe-109">Negli argomenti seguenti vengono illustrati i requisiti e le strategie necessari per la definizione delle proprietà e dei gestori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5cffe-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="5cffe-110">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="5cffe-111">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="5cffe-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="5cffe-112">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="5cffe-113">Inizializzazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="5cffe-114">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="5cffe-115">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="5cffe-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cffe-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cffe-117">Creazione di proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="5cffe-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="5cffe-118">Schema Descrizione proprietà</span><span class="sxs-lookup"><span data-stu-id="5cffe-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
