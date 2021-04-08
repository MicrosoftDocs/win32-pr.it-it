---
title: WM/ContainerFormat
description: L'attributo WM/ContainerFormat specifica il tipo di file caricato nell'oggetto chiamante.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato di Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718592"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="4e965-104">WM/ContainerFormat</span><span class="sxs-lookup"><span data-stu-id="4e965-104">WM/ContainerFormat</span></span>

<span data-ttu-id="4e965-105">L'attributo **WM/containerFormat** specifica il tipo di file caricato nell'oggetto chiamante.</span><span class="sxs-lookup"><span data-stu-id="4e965-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4e965-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="4e965-106">Global Constant</span></span>

<span data-ttu-id="4e965-107">g \_ wszWMContainerFormat</span><span class="sxs-lookup"><span data-stu-id="4e965-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="4e965-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4e965-108">Data Type</span></span>

<span data-ttu-id="4e965-109">[**WMT \_ \_formato di archiviazione**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ \_ binario di tipo WMT**)</span><span class="sxs-lookup"><span data-stu-id="4e965-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="4e965-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e965-110">Remarks</span></span>

<span data-ttu-id="4e965-111">Questo attributo viene usato al posto di **IWMProfile3:: GetStorageFormat** e **IWMProfile3:: SetStorageFormat**, che non sono più supportati.</span><span class="sxs-lookup"><span data-stu-id="4e965-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="4e965-112">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="4e965-112">This is a coded attribute.</span></span>

<span data-ttu-id="4e965-113">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="4e965-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="4e965-114">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4e965-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e965-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e965-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e965-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="4e965-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




