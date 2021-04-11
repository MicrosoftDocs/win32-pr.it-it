---
description: La tabella MIME associa un tipo di contenuto MIME con un'estensione di file o un CLSID per generare le informazioni sull'estensione o sul server COM richieste per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabella MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232850"
---
# <a name="mime-table"></a><span data-ttu-id="7359b-103">Tabella MIME</span><span class="sxs-lookup"><span data-stu-id="7359b-103">MIME Table</span></span>

<span data-ttu-id="7359b-104">La tabella MIME associa un tipo di contenuto MIME con un'estensione di file o un CLSID per generare le informazioni sull'estensione o sul server COM richieste per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="7359b-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="7359b-105">La tabella MIME contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="7359b-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="7359b-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="7359b-106">Column</span></span>      | <span data-ttu-id="7359b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7359b-107">Type</span></span>             | <span data-ttu-id="7359b-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="7359b-108">Key</span></span> | <span data-ttu-id="7359b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7359b-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="7359b-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="7359b-110">ContentType</span></span> | [<span data-ttu-id="7359b-111">Text</span><span class="sxs-lookup"><span data-stu-id="7359b-111">Text</span></span>](text.md) | <span data-ttu-id="7359b-112">S</span><span class="sxs-lookup"><span data-stu-id="7359b-112">Y</span></span>   | <span data-ttu-id="7359b-113">N</span><span class="sxs-lookup"><span data-stu-id="7359b-113">N</span></span>        |
| <span data-ttu-id="7359b-114">Estensione\_</span><span class="sxs-lookup"><span data-stu-id="7359b-114">Extension\_</span></span> | [<span data-ttu-id="7359b-115">Text</span><span class="sxs-lookup"><span data-stu-id="7359b-115">Text</span></span>](text.md) | <span data-ttu-id="7359b-116">N</span><span class="sxs-lookup"><span data-stu-id="7359b-116">N</span></span>   | <span data-ttu-id="7359b-117">N</span><span class="sxs-lookup"><span data-stu-id="7359b-117">N</span></span>        |
| <span data-ttu-id="7359b-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="7359b-118">CLSID</span></span>       | [<span data-ttu-id="7359b-119">GUID</span><span class="sxs-lookup"><span data-stu-id="7359b-119">GUID</span></span>](guid.md) | <span data-ttu-id="7359b-120">N</span><span class="sxs-lookup"><span data-stu-id="7359b-120">N</span></span>   | <span data-ttu-id="7359b-121">S</span><span class="sxs-lookup"><span data-stu-id="7359b-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7359b-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="7359b-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7359b-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="7359b-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="7359b-124">Questa colonna è un identificatore per il contenuto MIME.</span><span class="sxs-lookup"><span data-stu-id="7359b-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="7359b-125">Viene in genere scritto in formato tipo/formato.</span><span class="sxs-lookup"><span data-stu-id="7359b-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="7359b-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Estensione\_</span><span class="sxs-lookup"><span data-stu-id="7359b-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="7359b-127">Questa colonna contiene l'estensione del server da associare al contenuto MIME, senza il punto.</span><span class="sxs-lookup"><span data-stu-id="7359b-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="7359b-128">Questa colonna è una chiave esterna nella [tabella di estensione](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="7359b-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="7359b-129">La tabella di estensione contiene informazioni sul server di estensione del nome file che vengono utilizzate come parte di un annuncio pubblicitario.</span><span class="sxs-lookup"><span data-stu-id="7359b-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="7359b-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="7359b-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="7359b-131">Questa colonna contiene il CLSID del server COM da associare al contenuto MIME.</span><span class="sxs-lookup"><span data-stu-id="7359b-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="7359b-132">Il CLSID in questa colonna può essere una chiave esterna nella [tabella della classe](class-table.md) oppure può essere un CLSID già esistente nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7359b-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="7359b-133">La tabella della classe contiene informazioni relative al server COM utilizzate come parte dell'annuncio.</span><span class="sxs-lookup"><span data-stu-id="7359b-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7359b-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="7359b-134">Remarks</span></span>

<span data-ttu-id="7359b-135">Questa tabella viene definita quando viene eseguita l'azione [RegisterMIMEInfo](registermimeinfo-action.md) o [UnregisterMIMEInfo](unregistermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7359b-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="7359b-136">In modalità di annuncio, l'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server dalla tabella MIME per cui è abilitata la funzionalità corrispondente.</span><span class="sxs-lookup"><span data-stu-id="7359b-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="7359b-137">In caso contrario, l'azione registra le informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente da installare.</span><span class="sxs-lookup"><span data-stu-id="7359b-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="7359b-138">L' [azione UnregisterMIMEInfo](unregistermimeinfo-action.md) Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7359b-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="7359b-139">L'azione annulla la registrazione delle informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="7359b-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="7359b-140">Convalida</span><span class="sxs-lookup"><span data-stu-id="7359b-140">Validation</span></span>

<dl>

[<span data-ttu-id="7359b-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="7359b-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7359b-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="7359b-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7359b-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="7359b-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="7359b-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="7359b-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



