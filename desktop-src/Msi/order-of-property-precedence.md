---
description: Il programma di installazione imposta le proprietà utilizzando il seguente ordine di precedenza. Un valore di proprietà in questo elenco può eseguire l'override di un valore che viene seguito e sottoposto a override da un valore che lo precede nell'elenco.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordine di precedenza delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319000"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="595f2-104">Ordine di precedenza delle proprietà</span><span class="sxs-lookup"><span data-stu-id="595f2-104">Order of Property Precedence</span></span>

<span data-ttu-id="595f2-105">Il programma di installazione imposta le proprietà utilizzando il seguente ordine di precedenza.</span><span class="sxs-lookup"><span data-stu-id="595f2-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="595f2-106">Un valore di proprietà in questo elenco può eseguire l'override di un valore che viene seguito e sottoposto a override da un valore che lo precede nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="595f2-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="595f2-107">Proprietà specificate dall'ambiente operativo.</span><span class="sxs-lookup"><span data-stu-id="595f2-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="595f2-108">[Proprietà pubbliche](public-properties.md) impostate nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="595f2-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="595f2-109">Proprietà pubbliche elencate da [**AdminProperties**](adminproperties.md) PropertySet durante un' [installazione amministrativa](administrative-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="595f2-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="595f2-110">Proprietà pubbliche o private impostate durante l'applicazione di una [*trasformazione*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="595f2-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="595f2-111">Proprietà pubblica o privata impostata mediante la creazione della [tabella delle proprietà](property-table.md) del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="595f2-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="595f2-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="595f2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="595f2-113">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="595f2-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



