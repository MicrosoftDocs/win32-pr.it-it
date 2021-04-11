---
title: Elemento Metadata (instrumentationManifest)
description: Contiene i valori globali a cui è possibile fare riferimento in altri manifesti.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog elemento dei metadati
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119038"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="8ba00-104">Elemento Metadata (instrumentationManifest)</span><span class="sxs-lookup"><span data-stu-id="8ba00-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="8ba00-105">Contiene i valori globali a cui è possibile fare riferimento in altri manifesti.</span><span class="sxs-lookup"><span data-stu-id="8ba00-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="8ba00-106">Per un esempio, vedere il file Winmeta.xml incluso nella \\ cartella di inclusione del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8ba00-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="8ba00-107">L'elemento **Metadata** viene definito dall'elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba00-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba00-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ba00-108">Remarks</span></span>

<span data-ttu-id="8ba00-109">Sebbene sia possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo utilizzerà. gli unici metadati riconosciuti dal servizio sono i metadati trovati nel file di Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="8ba00-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba00-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ba00-110">Requirements</span></span>



| <span data-ttu-id="8ba00-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba00-111">Requirement</span></span> | <span data-ttu-id="8ba00-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8ba00-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ba00-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ba00-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba00-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ba00-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ba00-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ba00-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba00-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ba00-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ba00-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ba00-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ba00-118">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="8ba00-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="8ba00-119">**instrumentationManifest**</span><span class="sxs-lookup"><span data-stu-id="8ba00-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





