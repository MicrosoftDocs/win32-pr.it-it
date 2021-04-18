---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Parole chiave Public PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320859"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="25b69-104">Parole chiave Public PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="25b69-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="25b69-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="25b69-105">This topic is not current.</span></span> <span data-ttu-id="25b69-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="25b69-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="25b69-107">Nella sezione seguente vengono specificati gli elementi configurabili dall'utente e le definizioni dei parametri che potrebbero essere applicabili a un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="25b69-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="25b69-108">Utilizzo degli elementi configurabili dall'utente</span><span class="sxs-lookup"><span data-stu-id="25b69-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="25b69-109">Gli elementi configurabili dall'utente rappresentano parole chiave pubbliche dello schema di stampa che possono essere visualizzate in un documento PrintCapabilities o in un oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="25b69-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="25b69-110">Sono progettate per rappresentare gli attributi di dispositivo configurabili supportati da un dispositivo specifico o comunicano l'intento dell'impostazione di stampa da un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="25b69-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="25b69-111">Gli elementi configurabili dall'utente possono fare riferimento a elementi di riferimento al parametro.</span><span class="sxs-lookup"><span data-stu-id="25b69-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="25b69-112">Per altre informazioni, vedere la sezione [elementi di riferimento del parametro](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="25b69-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="25b69-113">Utilizzo delle definizioni dei parametri</span><span class="sxs-lookup"><span data-stu-id="25b69-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="25b69-114">Le definizioni dei parametri hanno il formato di tipi di elemento ParameterDef in un documento sulle funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="25b69-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="25b69-115">I tipi di elemento ParameterDef vengono inizializzati in un oggetto PrintTicket usando il tipo di elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="25b69-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="25b69-116">Il valore del parametro verrà specificato utilizzando l'elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="25b69-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="25b69-117">Una parola chiave configurabile dall'utente può fare riferimento a una definizione di parametro usando il tipo di elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="25b69-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="25b69-118">Per altre informazioni, vedere la sezione [costrutti di parametri](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="25b69-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25b69-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25b69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25b69-120">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="25b69-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



