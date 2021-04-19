---
description: Imposta l'identificatore di sicurezza radice per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332665"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="77187-103">MFPKEY \_ http \_ ByteStream \_ Urlmon \_ sicurezza \_ ID proprietà</span><span class="sxs-lookup"><span data-stu-id="77187-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="77187-104">Imposta l'identificatore di sicurezza radice per il flusso di byte HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="77187-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="77187-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="77187-105">Data type</span></span>

<span data-ttu-id="77187-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="77187-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="77187-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="77187-107">PROPVARIANT member</span></span>

<span data-ttu-id="77187-108">**Campo CAUB**</span><span class="sxs-lookup"><span data-stu-id="77187-108">**CAUB**</span></span>

<span data-ttu-id="77187-109">VT \_ vettore \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="77187-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="77187-110">**Campo CAUB**</span><span class="sxs-lookup"><span data-stu-id="77187-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="77187-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="77187-111">Remarks</span></span>

<span data-ttu-id="77187-112">Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="77187-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="77187-113">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="77187-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="77187-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="77187-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="77187-115">Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="77187-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="77187-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77187-116">Requirements</span></span>



| <span data-ttu-id="77187-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77187-117">Requirement</span></span> | <span data-ttu-id="77187-118">Valore</span><span class="sxs-lookup"><span data-stu-id="77187-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77187-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77187-119">Header</span></span><br/> | <dl> <span data-ttu-id="77187-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77187-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77187-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77187-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77187-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77187-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
