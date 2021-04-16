---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Aggiunta di istanze di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401836"
---
# <a name="adding-property-instances"></a><span data-ttu-id="f8692-104">Aggiunta di istanze di proprietà</span><span class="sxs-lookup"><span data-stu-id="f8692-104">Adding Property Instances</span></span>

<span data-ttu-id="f8692-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f8692-105">This topic is not current.</span></span> <span data-ttu-id="f8692-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f8692-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f8692-107">Lo schema di stampa consente la presenza di istanze di proprietà in un'istanza di Option.</span><span class="sxs-lookup"><span data-stu-id="f8692-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="f8692-108">Le istanze di proprietà definite nel documento PrintCapabilities non vengono propagate alle istanze delle opzioni salvate nel PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="f8692-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="f8692-109">Gli elementi proprietà non influiscono sul risultato del processo di assegnazione dei punteggi quando vengono confrontate due istanze di opzioni, ma le istanze di ScoredProperty influiscono su questo processo.</span><span class="sxs-lookup"><span data-stu-id="f8692-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="f8692-110">Tutti i driver di dispositivo che implementano un algoritmo di assegnazione dei punteggi devono osservare questa convenzione.</span><span class="sxs-lookup"><span data-stu-id="f8692-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="f8692-111">Ai provider PrintCapabilities è consentito aggiungere istanze di proprietà a un'opzione se tali istanze sono specifiche di questa particolare opzione e non altre, oppure se il provider intende visualizzare il valore di questa proprietà per ogni opzione della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f8692-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="f8692-112">Si supponga, ad esempio, che la proprietà PrintRate dipenda dall'opzione selezionata per la funzionalità PageResolution.</span><span class="sxs-lookup"><span data-stu-id="f8692-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="f8692-113">Se la proprietà PrintRate è stata posizionata al livello radice del documento PrintCapabilities, sarà a valore singolo e rifletterà solo la velocità di stampa per la risoluzione attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="f8692-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="f8692-114">Tuttavia, se la proprietà PrintRate è stata inserita all'interno di ogni opzione PageResolution, ogni istanza della proprietà PrintRate potrebbe riflettere la velocità di stampa per l'opzione PageResolution che lo conteneva.</span><span class="sxs-lookup"><span data-stu-id="f8692-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="f8692-115">Il documento PrintCapabilities conterrebbe più definizioni per PrintRate, una corrispondente a ogni opzione PageResolution.</span><span class="sxs-lookup"><span data-stu-id="f8692-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="f8692-116">Utilizzando una rappresentazione abbreviata, l'oggetto PrintCapabilities conterrebbe:</span><span class="sxs-lookup"><span data-stu-id="f8692-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="f8692-117">In alcune situazioni, l'inserimento di una proprietà della frequenza di stampa all'interno di ogni opzione di risoluzione è più utile per il client, perché il client può determinare a colpo d'occhio l'effetto di ogni opzione di risoluzione sulla frequenza di stampa, senza dover ottenere un nuovo documento PrintCapabilities per ogni impostazione di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="f8692-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="f8692-118">Si noti inoltre che anche le istanze di proprietà possono essere aggiunte come elementi figlio di elementi Feature.</span><span class="sxs-lookup"><span data-stu-id="f8692-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="f8692-119">Questa operazione è utile se sono presenti istanze di proprietà o valori di istanze di proprietà specifiche di ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f8692-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="f8692-120">Ad esempio, potrebbe essere presente una proprietà che specifica se è consentita la selezione di una sola opzione alla volta per una funzionalità o se è possibile selezionare più opzioni.</span><span class="sxs-lookup"><span data-stu-id="f8692-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="f8692-121">Questa è la scelta selezionata \_ . scegliere \_ molti proprietà usati nei file PPD e GPD.</span><span class="sxs-lookup"><span data-stu-id="f8692-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="f8692-122">Poiché alcune istanze della funzionalità possono essere identificate come PICK \_ One, mentre altre possono essere identificate come pick \_ many, questa proprietà deve essere definita per ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f8692-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="f8692-123">L'individuazione della proprietà come elemento figlio della funzionalità produce l'associazione tra la proprietà e la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f8692-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8692-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8692-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8692-125">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f8692-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



