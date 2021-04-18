---
title: Is_Protected
description: L' \_ attributo is protected è un attributo a livello di file che specifica se il contenuto del file è stato protetto mediante Digital Rights Management (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected formato Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299380"
---
# <a name="is_protected"></a><span data-ttu-id="759f8-104">\_Protetto</span><span class="sxs-lookup"><span data-stu-id="759f8-104">Is\_Protected</span></span>

<span data-ttu-id="759f8-105">L'attributo **is \_ protected** è un attributo a livello di file che specifica se il contenuto del file è stato protetto mediante Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="759f8-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="759f8-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="759f8-106">Global Constant</span></span>

<span data-ttu-id="759f8-107">g \_ wszWMProtected</span><span class="sxs-lookup"><span data-stu-id="759f8-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="759f8-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="759f8-108">Data Type</span></span>

<span data-ttu-id="759f8-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="759f8-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="759f8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="759f8-110">Remarks</span></span>

<span data-ttu-id="759f8-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="759f8-111">This is a coded attribute.</span></span> <span data-ttu-id="759f8-112">Il recupero di questa proprietà fornisce le stesse informazioni della chiamata a [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span><span class="sxs-lookup"><span data-stu-id="759f8-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="759f8-113">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="759f8-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="759f8-114">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="759f8-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="759f8-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="759f8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759f8-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="759f8-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




