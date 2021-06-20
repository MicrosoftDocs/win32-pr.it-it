---
description: Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Oggetti e nomi definiti nelle parole chiave dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408554"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="b8bef-103">Oggetti e nomi definiti nelle parole chiave dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b8bef-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="b8bef-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b8bef-104">This topic is not current.</span></span> <span data-ttu-id="b8bef-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b8bef-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b8bef-106">Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8bef-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="b8bef-107">Sono inclusi elementi come Feature, Option e ScoredProperty. nomi di attributo, ad esempio nome e propagazione; i valori e per gli attributi XML, ad esempio constrained.</span><span class="sxs-lookup"><span data-stu-id="b8bef-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="b8bef-108">In altre parole, ogni uso di un nome definito nelle parole chiave dello schema di stampa deve essere qualificato in modo esplicito con questo spazio dei nomi o deve essere associato in modo implicito a questo spazio dei nomi tramite un attributo xmlns predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8bef-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="b8bef-109">Il documento Parole chiave dello schema di stampa definisce le istanze dell'elemento pubblico che possono essere visualizzate in qualsiasi contesto o percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b8bef-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="b8bef-110">Le istanze degli elementi devono essere visualizzate solo all'interno del contesto o della posizione designata in Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="b8bef-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="b8bef-111">Ad esempio, l'istanza di <psf:Option name= "psk:Letter"> definita nelle parole chiave dello schema di stampa deve essere presente all'interno dell'istanza di <psf:Feature name = "psk:PageMediaSize"> (definita anche nelle parole chiave dello schema di stampa).</span><span class="sxs-lookup"><span data-stu-id="b8bef-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="b8bef-112">Non è possibile usare un'istanza Option specificata al di fuori del contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="b8bef-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="b8bef-113">Le istanze di elemento definite privatamente possono essere visualizzate ovunque, purché il tipo di elemento venga visualizzato in un contesto consentito dal framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8bef-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8bef-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8bef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8bef-115">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b8bef-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



