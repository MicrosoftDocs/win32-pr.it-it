---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Parole chiave pubbliche dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321014"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="09585-104">Parole chiave pubbliche dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="09585-104">Print Schema Public Keywords</span></span>

<span data-ttu-id="09585-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="09585-105">This topic is not current.</span></span> <span data-ttu-id="09585-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="09585-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="09585-107">Nella sezione seguente vengono specificate le parole chiave pubbliche definite per lo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="09585-107">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="09585-108">Utilizzo delle parole chiave pubbliche dello schema di stampa per le funzionalità di stampa</span><span class="sxs-lookup"><span data-stu-id="09585-108">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="09585-109">Le parole chiave specificate nelle parole chiave Public PrintCapabilities possono essere visualizzate in un documento sulle funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="09585-109">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="09585-110">Per ulteriori informazioni sul modo in cui queste parole chiave interagiscono con la tecnologia PrintCapabilities, vedere [Cenni preliminari](overview-of-the-printcapabilities.md) sulla sezione PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="09585-110">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="09585-111">Le parole chiave pubbliche specifiche per PrintTicket non devono essere visualizzate in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="09585-111">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="09585-112">Utilizzo delle parole chiave pubbliche dello schema di stampa per PrintTicket</span><span class="sxs-lookup"><span data-stu-id="09585-112">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="09585-113">Le parole chiave specificate in PrintTicket Public Keywords possono essere visualizzate in un oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="09585-113">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="09585-114">Le parole chiave PrintTicket vengono implementate come tipo di elemento Property.</span><span class="sxs-lookup"><span data-stu-id="09585-114">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="09585-115">Per ulteriori informazioni sul modo in cui queste parole chiave interagiscono con la tecnologia PrintTicket, vedere la sezione [informazioni di configurazione non correlate a PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="09585-115">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="09585-116">Le parole chiave specificate in PrintCapabilities Public Keywords possono essere visualizzate in un oggetto PrintTicket a seconda dell'implementazione di PrintTicket in un'applicazione e/o in un driver.</span><span class="sxs-lookup"><span data-stu-id="09585-116">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="09585-117">In questo modo vengono fornite le selezioni per gli attributi del dispositivo definiti nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="09585-117">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="09585-118">Per ulteriori informazioni sull'interazione tra le parole chiave PrintCapabilities e l'oggetto PrintTicket, consultare lo [scopo della sezione PrintTicket](purpose-of-the-printticket.md) .</span><span class="sxs-lookup"><span data-stu-id="09585-118">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09585-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09585-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09585-120">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="09585-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



