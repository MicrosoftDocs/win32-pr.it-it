---
description: Questo articolo specifica le parole chiave pubbliche definite per lo schema di stampa e il relativo utilizzo per PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Parole chiave pubbliche dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407144"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="a8ffd-103">Parole chiave pubbliche dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a8ffd-103">Print Schema Public Keywords</span></span>

<span data-ttu-id="a8ffd-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-104">This topic is not current.</span></span> <span data-ttu-id="a8ffd-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a8ffd-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8ffd-106">Nella sezione seguente vengono specificate le parole chiave pubbliche definite per lo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-106">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="a8ffd-107">Utilizzo delle parole chiave pubbliche dello schema di stampa per le funzionalità di stampa</span><span class="sxs-lookup"><span data-stu-id="a8ffd-107">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="a8ffd-108">Le parole chiave specificate in Parole chiave pubbliche PrintCapabilities POSSONO essere visualizzate in un documento di funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-108">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="a8ffd-109">Per altre informazioni sull'interazione di queste parole chiave con la tecnologia PrintCapabilities, vedere [Panoramica della sezione PrintCapabilities.](overview-of-the-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="a8ffd-109">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="a8ffd-110">Le parole chiave pubbliche specifiche di PrintTicket NON DOVREBBERO essere visualizzate in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-110">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="a8ffd-111">Utilizzo delle parole chiave pubbliche dello schema di stampa per PrintTicket</span><span class="sxs-lookup"><span data-stu-id="a8ffd-111">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="a8ffd-112">Le parole chiave specificate in Parole chiave pubbliche di PrintTicket possono essere visualizzate in un printticket.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-112">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="a8ffd-113">Le parole chiave PrintTicket vengono implementate come tipo di elemento Property.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-113">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="a8ffd-114">Per altre informazioni sull'interazione di queste parole chiave con la tecnologia PrintTicket, vedere la sezione Informazioni di configurazione [non correlate a PrintCapabilities.](configuration-information-not-related-to-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="a8ffd-114">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="a8ffd-115">Le parole chiave specificate in Parole chiave pubbliche PrintCapabilities POSSONO essere visualizzate in un PrintTicket a seconda dell'implementazione di PrintTicket in un'applicazione e/o in un driver.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-115">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="a8ffd-116">In questo modo vengono fornite le selezioni per gli attributi del dispositivo definiti nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a8ffd-116">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="a8ffd-117">Per altre informazioni sull'interazione tra le parole chiave PrintCapabilities e PrintTicket, vedere [scopo della sezione PrintTicket.](purpose-of-the-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="a8ffd-117">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8ffd-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8ffd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ffd-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a8ffd-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



