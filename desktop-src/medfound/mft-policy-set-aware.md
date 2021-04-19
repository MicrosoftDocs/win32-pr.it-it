---
description: Specifica se IMFTransform vuole ricevere notifiche di completamento MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310211"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="29dbe-103">\_ \_ Attributo Aware del set di criteri MFT \_</span><span class="sxs-lookup"><span data-stu-id="29dbe-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="29dbe-104">Se diverso da zero, indica che **IMFTransform** desidera ricevere notifiche di completamento [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="29dbe-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="29dbe-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="29dbe-105">Data type</span></span>

<span data-ttu-id="29dbe-106">**UInt32** (considerato **bool**)</span><span class="sxs-lookup"><span data-stu-id="29dbe-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="29dbe-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="29dbe-107">Get/set</span></span>

<span data-ttu-id="29dbe-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="29dbe-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="29dbe-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="29dbe-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="29dbe-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="29dbe-110">Applies to</span></span>

[<span data-ttu-id="29dbe-111">**IMFInputTrustAuthority**</span><span class="sxs-lookup"><span data-stu-id="29dbe-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="29dbe-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="29dbe-112">Remarks</span></span>

<span data-ttu-id="29dbe-113">Questo attributo può essere usato da un **IMFInputTrustAuthority** Decrypter.</span><span class="sxs-lookup"><span data-stu-id="29dbe-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="29dbe-114">Un'implementazione di un modulo di decrittografia del contenuto (CDM) può includere un'implementazione di **IMFInputTrustAuthority**.</span><span class="sxs-lookup"><span data-stu-id="29dbe-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="29dbe-115">È possibile accedere all'oggetto **IMFInputTrustAuthority** tramite [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="29dbe-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="29dbe-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="29dbe-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="29dbe-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29dbe-117">Requirements</span></span>



| <span data-ttu-id="29dbe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29dbe-118">Requirement</span></span> | <span data-ttu-id="29dbe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="29dbe-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29dbe-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29dbe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29dbe-121">Aggiornamento di Windows 10 aprile 2020</span><span class="sxs-lookup"><span data-stu-id="29dbe-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="29dbe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29dbe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29dbe-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="29dbe-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29dbe-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29dbe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29dbe-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29dbe-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="29dbe-126">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="29dbe-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
