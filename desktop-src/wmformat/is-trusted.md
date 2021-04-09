---
title: Is_Trusted
description: L' \_ attributo is trusted è un attributo a livello di file che specifica se l'URL di acquisizione della licenza nel file è attendibile.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted formato Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956018"
---
# <a name="is_trusted"></a><span data-ttu-id="c1f65-104">\_Attendibile</span><span class="sxs-lookup"><span data-stu-id="c1f65-104">Is\_Trusted</span></span>

<span data-ttu-id="c1f65-105">L'attributo **is \_ Trusted** è un attributo a livello di file che specifica se l'URL di acquisizione della licenza nel file è attendibile.</span><span class="sxs-lookup"><span data-stu-id="c1f65-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c1f65-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="c1f65-106">Global Constant</span></span>

<span data-ttu-id="c1f65-107">g \_ wszWMTrusted</span><span class="sxs-lookup"><span data-stu-id="c1f65-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="c1f65-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c1f65-108">Data Type</span></span>

<span data-ttu-id="c1f65-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c1f65-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f65-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1f65-110">Remarks</span></span>

<span data-ttu-id="c1f65-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="c1f65-111">This is a coded attribute.</span></span>

<span data-ttu-id="c1f65-112">Prima di passare a un URL di acquisizione della licenza contenuto in un file protetto da DRM, un'applicazione deve prima verificare che la proprietà sia true.</span><span class="sxs-lookup"><span data-stu-id="c1f65-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="c1f65-113">Se è false, l'applicazione deve notificare all'utente che è possibile che l'URL sia stato alterato.</span><span class="sxs-lookup"><span data-stu-id="c1f65-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="c1f65-114">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="c1f65-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="c1f65-115">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="c1f65-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1f65-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1f65-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f65-117">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="c1f65-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




