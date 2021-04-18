---
description: Consente all'Microsoft Media Foundation flusso di byte HTTP di utilizzare i moniker URL (detti anche Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Proprietà MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325421"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="80726-103">MFPKEY \_ http \_ ByteStream \_ Abilita \_ Proprietà Urlmon</span><span class="sxs-lookup"><span data-stu-id="80726-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="80726-104">Consente all'Microsoft Media Foundation flusso di byte HTTP di utilizzare i moniker URL (detti anche *Urlmon*).</span><span class="sxs-lookup"><span data-stu-id="80726-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="80726-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="80726-105">Data type</span></span>

<span data-ttu-id="80726-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="80726-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="80726-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="80726-107">PROPVARIANT member</span></span>

<span data-ttu-id="80726-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="80726-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="80726-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="80726-109">VT\_BOOL</span></span>

<span data-ttu-id="80726-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="80726-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="80726-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="80726-111">Remarks</span></span>

<span data-ttu-id="80726-112">Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="80726-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="80726-113">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="80726-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="80726-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="80726-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="80726-115">Se il valore è **Variant \_ true**, il flusso di byte http USA Urlmon per il trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="80726-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="80726-116">In caso contrario, se il valore è **Variant \_ false**, il flusso di byte utilizza WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="80726-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="80726-117">Il valore predefinito è **Variant \_ true** per le applicazioni Windows Store e **Variant \_ false** per applicazioni desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="80726-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="80726-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80726-118">Requirements</span></span>



| <span data-ttu-id="80726-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="80726-119">Requirement</span></span> | <span data-ttu-id="80726-120">Valore</span><span class="sxs-lookup"><span data-stu-id="80726-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80726-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80726-121">Header</span></span><br/> | <dl> <span data-ttu-id="80726-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80726-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80726-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80726-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80726-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80726-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
