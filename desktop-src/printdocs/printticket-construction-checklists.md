---
description: Vedere come l'autore di un client PrintTicket può usare i tipi di elemento per creare un oggetto PrintTicket che descrive le finalità per un dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Elenchi di controllo per la costruzione di PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405474"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="c4cfa-103">Elenchi di controllo per la costruzione di PrintTicket</span><span class="sxs-lookup"><span data-stu-id="c4cfa-103">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="c4cfa-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-104">This topic is not current.</span></span> <span data-ttu-id="c4cfa-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4cfa-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4cfa-106">Questa sezione illustra come l'autore di un client PrintTicket può usare i tipi di elemento definiti in Print Schema Framework per creare un printTicket che descrive le finalità per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-106">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="c4cfa-107">PrintTicket può essere generico (non associato a un dispositivo specifico) o può essere specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-107">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="c4cfa-108">La semantica di PrintTicket viene presentata in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-108">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="c4cfa-109">Questa sezione contiene anche una panoramica dei concetti e della terminologia trattati in modo più approfondito nelle sezioni successive.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-109">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="c4cfa-110">Esistono due approcci fondamentalmente diversi per la costruzione di un oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-110">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="c4cfa-111">È possibile usare entrambi gli approcci.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-111">Either approach can be used.</span></span>

-   <span data-ttu-id="c4cfa-112">Impostare come destinazione PrintTicket un dispositivo sconosciuto o generico [creando un printTicket generico.](creating-a-generic-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="c4cfa-112">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="c4cfa-113">Se l'obiettivo principale è mantenere la finalità dell'utente finale, è possibile adottare questo approccio, creando e archiviando un PrintTicket generico non convalidato con il documento.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-113">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="c4cfa-114">Impostare come destinazione PrintTicket un dispositivo specifico, creando [un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="c4cfa-114">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="c4cfa-115">Se si è più interessati a sfruttare tutte le funzionalità offerte da un particolare dispositivo, è possibile adottare questo approccio, creando un PrintTicket per il dispositivo specifico e archiviando il PrintTicket convalidato con il documento.</span><span class="sxs-lookup"><span data-stu-id="c4cfa-115">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4cfa-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4cfa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4cfa-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c4cfa-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



