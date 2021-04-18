---
description: Imposta l'ID chiave per l'esempio.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Attributo MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310244"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="f9338-103">MFSampleExtension \_ Content \_ keyId-attributo</span><span class="sxs-lookup"><span data-stu-id="f9338-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="f9338-104">Imposta l'ID chiave per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="f9338-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9338-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f9338-105">Data type</span></span>

<span data-ttu-id="f9338-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f9338-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="f9338-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9338-107">Examples</span></span>

<span data-ttu-id="f9338-108">Nell'esempio seguente viene illustrato come impostare l'ID chiave per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="f9338-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="f9338-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9338-109">Requirements</span></span>



| <span data-ttu-id="f9338-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9338-110">Requirement</span></span> | <span data-ttu-id="f9338-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f9338-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9338-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9338-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f9338-113">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f9338-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f9338-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9338-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f9338-115">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f9338-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f9338-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9338-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9338-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9338-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9338-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9338-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9338-119">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9338-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9338-120">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f9338-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="f9338-121">\_SubSampleMappingSplit di crittografia MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="f9338-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




