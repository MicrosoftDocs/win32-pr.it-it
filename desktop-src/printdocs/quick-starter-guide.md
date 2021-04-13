---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guida introduttiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f3933cb59e270dd8ef2eff8d295d33ab1f9203
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351776"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="e096f-104">Guida introduttiva</span><span class="sxs-lookup"><span data-stu-id="e096f-104">Quick Starter Guide</span></span>

<span data-ttu-id="e096f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e096f-105">This topic is not current.</span></span> <span data-ttu-id="e096f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e096f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e096f-107">Questa pagina è stata progettata per fornire una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096f-107">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="e096f-108">Anche se si consiglia di leggere la specifica dello schema di stampa in modo completo, questa pagina consentirà di iniziare subito a fare un salto in aree principali a cui è necessario prestare attenzione.</span><span class="sxs-lookup"><span data-stu-id="e096f-108">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="e096f-109">Leggi le [tecnologie Schema-Related di stampa](print-schema-related-technologies.md) per offrire una panoramica delle tecnologie di PrintTicket e delle funzionalità di stampa</span><span class="sxs-lookup"><span data-stu-id="e096f-109">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="e096f-110">Assicurarsi di disporre di una stretta sul [Riepilogo dei tipi di elemento](summary-of-element-types.md) utilizzati per esprimere le tecnologie correlate allo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="e096f-110">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="e096f-111">I documenti e gli PrintTicket PrintCapabilities sono definiti in tre livelli di prefisso, processo, documento e pagina di [ambito](scoping-prefix.md) .</span><span class="sxs-lookup"><span data-stu-id="e096f-111">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="e096f-112">Lettura dei diversi [attributi XML](xml-attributes.md) utilizzati all'interno di diversi tipi di elementi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e096f-112">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="e096f-113">Esaminare l' [elenco di controllo per la costruzione di documenti PrintCapabilities](printcapabilities-document-construction-checklist.md) e anche l' [esempio di documento PrintCapabilities](printcapabilities-document-example.md) fornito</span><span class="sxs-lookup"><span data-stu-id="e096f-113">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="e096f-114">Esaminare gli [elenchi di controllo di costruzione PrintTicket](printticket-construction-checklists.md) e anche l' [esempio PrintTicket](printticket-example.md) fornito</span><span class="sxs-lookup"><span data-stu-id="e096f-114">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="e096f-115">I provider PrintTicket devono inoltre esaminare l' [elenco di controllo di convalida PrintTicket](printticket-validation-checklist.md) per garantire la conformità con la specifica PrintSchema</span><span class="sxs-lookup"><span data-stu-id="e096f-115">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="e096f-116">Esaminare [gli elementi configurabili dall'utente](user-configurable-elements.md) e le [definizioni di parametri](parameter-definitions.md) public Print Schema parole chiave che possono essere visualizzate in un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e096f-116">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="e096f-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e096f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e096f-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e096f-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



