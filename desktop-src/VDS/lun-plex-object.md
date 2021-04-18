---
description: Oggetto PLEX LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Oggetto PLEX LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318596"
---
# <a name="lun-plex-object"></a><span data-ttu-id="06a2f-103">Oggetto PLEX LUN</span><span class="sxs-lookup"><span data-stu-id="06a2f-103">LUN Plex Object</span></span>

<span data-ttu-id="06a2f-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06a2f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="06a2f-105">Un oggetto PLEX LUN modella un PLEX LUN contenuto in un LUN.</span><span class="sxs-lookup"><span data-stu-id="06a2f-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="06a2f-106">Solo un LUN con mirroring può avere più Plex; tutti gli altri tipi LUN hanno un plex.</span><span class="sxs-lookup"><span data-stu-id="06a2f-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="06a2f-107">Ogni plex contiene una copia dei dati nel LUN.</span><span class="sxs-lookup"><span data-stu-id="06a2f-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="06a2f-108">È possibile aggiungere nuovi Plex a un LUN e, ad eccezione del Plex originale, i plex esistenti possono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="06a2f-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="06a2f-109">VDS supporta quattro tipi di PLEX LUN: semplici, con spanning, con striping e con striping con parità.</span><span class="sxs-lookup"><span data-stu-id="06a2f-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="06a2f-110">Per una descrizione di ognuno di questi tipi LUN, vedere l' [oggetto lun](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="06a2f-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="06a2f-111">Usare il metodo [**IVdsLun:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) per aggiungere un plex a un LUN e il metodo [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) per eliminare il plex.</span><span class="sxs-lookup"><span data-stu-id="06a2f-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="06a2f-112">È possibile eseguire una query per i PLEX LUN richiamando il metodo [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) .</span><span class="sxs-lookup"><span data-stu-id="06a2f-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="06a2f-113">È possibile ottenere un puntatore a un PLEX LUN specifico selezionando l'oggetto Plex desiderato dall'enumerazione restituita dal metodo **QueryPlexes** .</span><span class="sxs-lookup"><span data-stu-id="06a2f-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="06a2f-114">Con un oggetto Plex è possibile eseguire una query per gli extent delle unità e i suggerimenti di automagic e applicare nuovi hint.</span><span class="sxs-lookup"><span data-stu-id="06a2f-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="06a2f-115">Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto LUN Plex includono il tipo di Plex, le dimensioni, lo stato, l'integrità, lo stato di transizione e i flag. elenco e dimensioni di striping senza maschera; e un'impostazione della priorità di ricompilazione.</span><span class="sxs-lookup"><span data-stu-id="06a2f-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="06a2f-116">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="06a2f-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="06a2f-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="06a2f-117">Type</span></span>                                              | <span data-ttu-id="06a2f-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="06a2f-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a2f-119">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="06a2f-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="06a2f-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="06a2f-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="06a2f-121">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="06a2f-121">Associated enumerations</span></span>                           | <span data-ttu-id="06a2f-122">[**VDS \_ LUN \_ Plex \_ flag**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS \_ lun \_ Plex \_ status**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)e [**VDS \_ lun \_ Plex \_ Type**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="06a2f-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="06a2f-123">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="06a2f-123">Associated structures</span></span>                             | <span data-ttu-id="06a2f-124">[**VDS \_ \_ \_ prop Plex di lun**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span><span class="sxs-lookup"><span data-stu-id="06a2f-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="06a2f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06a2f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a2f-126">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="06a2f-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="06a2f-127">LUN (oggetto)</span><span class="sxs-lookup"><span data-stu-id="06a2f-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
