---
description: Informazioni sul riferimento ai parametri e all'elemento ParameterDef. Un esempio di opzione che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzato.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Riferimento ai parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405324"
---
# <a name="referencing-parameters"></a><span data-ttu-id="2391d-104">Riferimento ai parametri</span><span class="sxs-lookup"><span data-stu-id="2391d-104">Referencing Parameters</span></span>

<span data-ttu-id="2391d-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="2391d-105">This topic is not current.</span></span> <span data-ttu-id="2391d-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2391d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2391d-107">Un esempio concreto di un'opzione che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2391d-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="2391d-108">Si noti che fa riferimento a due parametri: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="2391d-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="2391d-109">Ogni istanza ParameterRef fa riferimento a un'istanza ParameterDef definita altrove nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2391d-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="2391d-110">Per informazioni sull'elemento ParameterDef, vedere [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="2391d-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="2391d-111">Per informazioni concettuali sulla definizione dei parametri, vedere [Elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="2391d-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="2391d-112">La semplice creazione di un'opzione con parametri non è sufficiente per garantire che l'opzione venga gestita ed elaborata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2391d-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="2391d-113">I client e il provider PrintCapabilities/PrintTicket devono fornire supporto aggiuntivo per implementare correttamente istanze Option con parametri.</span><span class="sxs-lookup"><span data-stu-id="2391d-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="2391d-114">I comportamenti necessari sono descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2391d-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2391d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2391d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2391d-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2391d-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



