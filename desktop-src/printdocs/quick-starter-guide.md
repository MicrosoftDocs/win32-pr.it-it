---
description: Questo articolo offre una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guida introduttiva rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6060de551d3fb663e148cf80f661c4d517a51b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405314"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="386e3-103">Guida introduttiva rapida</span><span class="sxs-lookup"><span data-stu-id="386e3-103">Quick Starter Guide</span></span>

<span data-ttu-id="386e3-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="386e3-104">This topic is not current.</span></span> <span data-ttu-id="386e3-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="386e3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="386e3-106">Questa pagina è progettata per offrire una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="386e3-106">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="386e3-107">Anche se è consigliabile leggere la specifica dello schema di stampa per intero, questa pagina consente di iniziare a fare un salto nelle aree chiave a cui prestare attenzione.</span><span class="sxs-lookup"><span data-stu-id="386e3-107">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="386e3-108">Leggere [print Schema-Related Technologies](print-schema-related-technologies.md) per una panoramica delle tecnologie PrintTicket e Print Capabilities</span><span class="sxs-lookup"><span data-stu-id="386e3-108">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="386e3-109">Assicurarsi di avere a portata di mano il riepilogo [dei tipi](summary-of-element-types.md) di elementi usati per esprimere le tecnologie correlate allo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="386e3-109">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="386e3-110">I documenti PrintCapabilities e PrintTicket [](scoping-prefix.md) sono definiti a tre livelli di prefisso di ambito, Job, Document e Page.</span><span class="sxs-lookup"><span data-stu-id="386e3-110">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="386e3-111">Leggere i diversi attributi [XML usati](xml-attributes.md) all'interno di diversi tipi di elementi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="386e3-111">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="386e3-112">Esaminare [l'elenco di controllo per la costruzione di documenti PrintCapabilities](printcapabilities-document-construction-checklist.md) e anche l'esempio [di documento PrintCapabilities fornito](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="386e3-112">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="386e3-113">Esaminare gli [elenchi di controllo per la costruzione di PrintTicket](printticket-construction-checklists.md) e anche l'esempio [printticket fornito](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="386e3-113">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="386e3-114">I provider PrintTicket devono anche esaminare [l'elenco di controllo di convalida PrintTicket](printticket-validation-checklist.md) per garantire la conformità alla specifica PrintSchema</span><span class="sxs-lookup"><span data-stu-id="386e3-114">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="386e3-115">Esaminare sia le parole [](parameter-definitions.md) [chiave dello](user-configurable-elements.md) schema di stampa pubbliche degli elementi configurabili dall'utente che le definizioni dei parametri che possono essere visualizzate in un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="386e3-115">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="386e3-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="386e3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="386e3-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="386e3-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



