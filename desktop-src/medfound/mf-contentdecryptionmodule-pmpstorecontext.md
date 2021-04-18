---
description: Specifica una stringa di contesto usata dalle implementazioni del modulo di decrittografia del contenuto (CDM) che usano MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309578"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="24101-103">\_ \_ Proprietà PMPSTORECONTEXT di MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="24101-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="24101-104">Specifica una stringa di contesto usata dalle implementazioni del modulo di decrittografia del contenuto (CDM) che usano [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span><span class="sxs-lookup"><span data-stu-id="24101-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="24101-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="24101-105">Data type</span></span>

<span data-ttu-id="24101-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="24101-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="24101-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="24101-107">Property GUID</span></span>

<span data-ttu-id="24101-108">**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**</span><span class="sxs-lookup"><span data-stu-id="24101-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="24101-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="24101-109">Property value</span></span>

<span data-ttu-id="24101-110">Stringa di contesto utilizzata dalle implementazioni del modulo di decrittografia del contenuto (CDM).</span><span class="sxs-lookup"><span data-stu-id="24101-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="24101-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="24101-111">Remarks</span></span>

<span data-ttu-id="24101-112">Il responsabile dell'implementazione CDM deve cercare questo valore e passare il valore al [Costruttore MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) usando il nome della proprietà "Windows. Media. Protection. PMPStoreContext".</span><span class="sxs-lookup"><span data-stu-id="24101-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="24101-113">Le app non devono creare questa proprietà quando viene chiamato [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="24101-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="24101-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24101-114">Requirements</span></span>



| <span data-ttu-id="24101-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24101-115">Requirement</span></span> | <span data-ttu-id="24101-116">Valore</span><span class="sxs-lookup"><span data-stu-id="24101-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24101-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24101-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24101-118">Aggiornamento di Windows 10 aprile 2020</span><span class="sxs-lookup"><span data-stu-id="24101-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="24101-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24101-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="24101-120"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="24101-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24101-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24101-121">See also</span></span>

- [<span data-ttu-id="24101-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24101-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="24101-123">MediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="24101-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




