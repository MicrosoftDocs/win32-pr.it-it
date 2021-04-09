---
title: Struttura STGMEDIUM
description: Struttura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104047578"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="9b852-103">Struttura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="9b852-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="9b852-104">Proprio come la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) rappresenta un miglioramento dell'identificatore di formato degli Appunti di Windows, pertanto la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) rappresenta un miglioramento dell'handle di memoria globale usato per trasferire i dati.</span><span class="sxs-lookup"><span data-stu-id="9b852-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="9b852-105">La struttura **STGMEDIUM** include un membro, **TYMED**, che indica il supporto da usare e un'Unione che comprende puntatori e un handle per ottenere qualsiasi valore medio specificato in **TYMED**.</span><span class="sxs-lookup"><span data-stu-id="9b852-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="9b852-106">La struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) consente a entrambe le origini dati e ai consumer di scegliere il supporto di scambio più efficiente in base al rendering.</span><span class="sxs-lookup"><span data-stu-id="9b852-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="9b852-107">Se i dati sono talmente grandi che devono essere conservati su disco, l'origine dati può indicare un supporto basato su disco nel formato preferito, usando solo la memoria globale come backup se è l'unico mezzo che il consumer riconosce.</span><span class="sxs-lookup"><span data-stu-id="9b852-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="9b852-108">La possibilità di usare il supporto migliore per gli scambi come impostazione predefinita migliora le prestazioni complessive dello scambio di dati tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9b852-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="9b852-109">Ad esempio, se alcuni dei dati da trasferire sono già su disco, l'applicazione di origine può spostarla o copiarla in una nuova destinazione, nella stessa applicazione o in un altro, senza dover prima caricare i dati nella memoria globale.</span><span class="sxs-lookup"><span data-stu-id="9b852-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="9b852-110">Al termine della ricezione, il consumer dei dati non deve riscriverlo sul disco.</span><span class="sxs-lookup"><span data-stu-id="9b852-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b852-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b852-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b852-112">Formati di dati e supporti di trasferimento</span><span class="sxs-lookup"><span data-stu-id="9b852-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




