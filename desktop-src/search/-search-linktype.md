---
description: Specifica il tipo di collegamento durante la ricerca per indicizzazione o l'indicizzazione.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumerazione LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306158"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="e4664-103">Enumerazione LINKTYPE</span><span class="sxs-lookup"><span data-stu-id="e4664-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="e4664-104">\[L'enumerazione **LinkType** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="e4664-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="e4664-105">Specifica il tipo di collegamento durante la ricerca per indicizzazione o l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="e4664-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4664-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4664-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="e4664-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="e4664-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4664-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL LinkType**</span><span class="sxs-lookup"><span data-stu-id="e4664-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="e4664-109">Specifica se il tipo di collegamento URL deve essere indicizzato.</span><span class="sxs-lookup"><span data-stu-id="e4664-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="e4664-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**contenuto di LINKTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e4664-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="e4664-111">Specifica se il contenuto del collegamento deve essere indicizzato.</span><span class="sxs-lookup"><span data-stu-id="e4664-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="e4664-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**correlate a LINKTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e4664-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="e4664-113">Specifica un collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e4664-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4664-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4664-114">Remarks</span></span>

<span data-ttu-id="e4664-115">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare i flag **LinkType** e le altre API seguenti: i metodi [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e la struttura [**LINKINFO**](-search-linkinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e4664-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4664-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4664-116">Requirements</span></span>



| <span data-ttu-id="e4664-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4664-117">Requirement</span></span> | <span data-ttu-id="e4664-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e4664-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4664-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4664-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4664-120">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4664-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e4664-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4664-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4664-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4664-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




