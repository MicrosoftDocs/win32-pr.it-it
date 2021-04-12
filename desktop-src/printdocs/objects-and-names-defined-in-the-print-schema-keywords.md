---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Oggetti e nomi definiti nelle parole chiave dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234557"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="a6795-104">Oggetti e nomi definiti nelle parole chiave dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a6795-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="a6795-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a6795-105">This topic is not current.</span></span> <span data-ttu-id="a6795-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a6795-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6795-107">Il Framework dello schema di stampa definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave Print Schema.</span><span class="sxs-lookup"><span data-stu-id="a6795-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="a6795-108">Sono inclusi elementi quali feature, Option e ScoredProperty; nomi di attributi, ad esempio nome e propagazione; valori e per gli attributi XML, ad esempio vincolato.</span><span class="sxs-lookup"><span data-stu-id="a6795-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="a6795-109">In altre parole, ogni utilizzo di un nome definito nelle parole chiave dello schema di stampa deve essere qualificato in modo esplicito con questo spazio dei nomi oppure deve essere associato in modo implicito a questo spazio dei nomi tramite l'utilizzo di un attributo xmlns predefinito.</span><span class="sxs-lookup"><span data-stu-id="a6795-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="a6795-110">Il documento parole chiave dello schema di stampa definisce le istanze di elementi pubblici che possono essere visualizzate in un contesto o in un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="a6795-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="a6795-111">Le istanze degli elementi devono essere visualizzate solo nel contesto o nel percorso designato nel Framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="a6795-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="a6795-112">Ad esempio, l'<PSF: Option Name = "PSK: Letter" > istanza definita nelle parole chiave Print Schema deve essere visualizzata all'interno dell'istanza di <PSF: feature name = "PSK: PageMediaSize" > (definita anche nelle parole chiave Print Schema).</span><span class="sxs-lookup"><span data-stu-id="a6795-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="a6795-113">Non si ha la libertà di usare un'istanza di opzione specificata al di fuori del contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="a6795-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="a6795-114">Le istanze degli elementi definite privatamente possono essere visualizzate in qualsiasi punto, purché il tipo di elemento venga visualizzato in un contesto consentito dal Framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="a6795-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6795-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6795-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6795-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a6795-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



