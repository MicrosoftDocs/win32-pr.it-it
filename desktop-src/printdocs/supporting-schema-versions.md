---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Supporto delle versioni dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d674449d581aca2ddfc80da2312b31eb6c930a6f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321035"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="9264e-104">Supporto delle versioni dello schema</span><span class="sxs-lookup"><span data-stu-id="9264e-104">Supporting Schema Versions</span></span>

<span data-ttu-id="9264e-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9264e-105">This topic is not current.</span></span> <span data-ttu-id="9264e-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9264e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9264e-107">Il Framework dello schema di stampa è soggetto a modifiche in futuro quando si verificano nuove esigenze.</span><span class="sxs-lookup"><span data-stu-id="9264e-107">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="9264e-108">Tali modifiche dovrebbero essere molto poco frequenti, perché la modifica più comune è l'introduzione di nuovi nomi di istanza.</span><span class="sxs-lookup"><span data-stu-id="9264e-108">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="9264e-109">Questa modifica non influisce sulla struttura del Framework e deve essere trasparente per i client e i provider.</span><span class="sxs-lookup"><span data-stu-id="9264e-109">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="9264e-110">Tutte le modifiche apportate alla struttura e all'organizzazione del Framework dello schema di stampa verranno identificate da incrementi al relativo numero di versione.</span><span class="sxs-lookup"><span data-stu-id="9264e-110">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="9264e-111">Le aggiunte alle parole chiave dello schema di stampa non verranno identificate.</span><span class="sxs-lookup"><span data-stu-id="9264e-111">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="9264e-112">I provider PrintTicket devono essere in grado di supportare la versione corrente di Print Schema Framework, nonché qualsiasi versione precedente.</span><span class="sxs-lookup"><span data-stu-id="9264e-112">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="9264e-113">La versione di Print Schema Framework viene identificata utilizzando l'attributo XML: Version visualizzata in corrispondenza dell'elemento radice dell'oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="9264e-113">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9264e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9264e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9264e-115">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9264e-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



