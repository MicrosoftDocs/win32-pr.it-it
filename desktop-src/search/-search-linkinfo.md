---
description: Archivia le informazioni sui tipi di collegamento e viene utilizzato dall'interfaccia IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Struttura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225955"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="98f12-103">Struttura LINKINFO</span><span class="sxs-lookup"><span data-stu-id="98f12-103">LINKINFO structure</span></span>

<span data-ttu-id="98f12-104">\[**LINKINFO** e [**IItemPreviewerExt**](-search-iitempreviewerext.md) sono supportati solo in Windows XP e Windows Server 2003 e non devono più essere utilizzati.\]</span><span class="sxs-lookup"><span data-stu-id="98f12-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="98f12-105">Archivia le informazioni sui tipi di collegamento e viene utilizzato dall'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) .</span><span class="sxs-lookup"><span data-stu-id="98f12-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f12-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98f12-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="98f12-107">Members</span><span class="sxs-lookup"><span data-stu-id="98f12-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="98f12-108">**type**</span><span class="sxs-lookup"><span data-stu-id="98f12-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-109">Tipo: **[ **LinkType**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="98f12-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-110">Tipo di collegamento specificato durante la ricerca per indicizzazione o l'indicizzazione indicata da una costante [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="98f12-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-111">**bstrContentType**</span><span class="sxs-lookup"><span data-stu-id="98f12-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98f12-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-113">Valore **BSTR** che specifica il tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="98f12-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-114">**bstrEncoding**</span><span class="sxs-lookup"><span data-stu-id="98f12-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98f12-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-116">Attributo EncodingStyle specificato nel file Web Services Description Language (WSDL).</span><span class="sxs-lookup"><span data-stu-id="98f12-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-117">**bstrFileExt**</span><span class="sxs-lookup"><span data-stu-id="98f12-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98f12-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-119">Valore **BSTR** che specifica l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="98f12-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-120">**varData**</span><span class="sxs-lookup"><span data-stu-id="98f12-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-121">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="98f12-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-122">Variant che specifica il valore della variabile.</span><span class="sxs-lookup"><span data-stu-id="98f12-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-123">**dwRelatedParts**</span><span class="sxs-lookup"><span data-stu-id="98f12-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="98f12-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-125">**DWORD** che specifica le parti correlate.</span><span class="sxs-lookup"><span data-stu-id="98f12-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-126">**bstrRelatedCid**</span><span class="sxs-lookup"><span data-stu-id="98f12-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98f12-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-128">Valore **BSTR** che specifica una proprietà CID, una stringa decimale non riempita e con segno.</span><span class="sxs-lookup"><span data-stu-id="98f12-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="98f12-129">**lCodePage**</span><span class="sxs-lookup"><span data-stu-id="98f12-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="98f12-130">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="98f12-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="98f12-131">Tabella codici da utilizzare per la codifica della stringa.</span><span class="sxs-lookup"><span data-stu-id="98f12-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98f12-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="98f12-132">Remarks</span></span>

<span data-ttu-id="98f12-133">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario utilizzare la struttura **LINKINFO** e le API seguenti: i metodi [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="98f12-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f12-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98f12-134">Requirements</span></span>



| <span data-ttu-id="98f12-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f12-135">Requirement</span></span> | <span data-ttu-id="98f12-136">Valore</span><span class="sxs-lookup"><span data-stu-id="98f12-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98f12-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98f12-137">Minimum supported client</span></span><br/> | <span data-ttu-id="98f12-138">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98f12-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98f12-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98f12-139">Minimum supported server</span></span><br/> | <span data-ttu-id="98f12-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="98f12-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98f12-141">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="98f12-141">Redistributable</span></span><br/>          | <span data-ttu-id="98f12-142">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="98f12-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




