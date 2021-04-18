---
description: Imposta i flag di associazione del moniker per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325417"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="648f5-103">MFPKEY \_ http \_ ByteStream \_ Urlmon \_ binding \_ Flags proprietà</span><span class="sxs-lookup"><span data-stu-id="648f5-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="648f5-104">Imposta i flag di associazione del moniker per il flusso di byte HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="648f5-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="648f5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="648f5-105">Data type</span></span>

<span data-ttu-id="648f5-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="648f5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="648f5-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="648f5-107">PROPVARIANT member</span></span>

<span data-ttu-id="648f5-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="648f5-108">**ULONG**</span></span>

<span data-ttu-id="648f5-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="648f5-109">VT\_UI4</span></span>

<span data-ttu-id="648f5-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="648f5-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="648f5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="648f5-111">Remarks</span></span>

<span data-ttu-id="648f5-112">Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="648f5-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="648f5-113">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="648f5-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="648f5-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="648f5-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="648f5-115">Il valore di questa proprietà è un operatore OR bit per bit di **flag dell'enumerazione** **BINDF** .</span><span class="sxs-lookup"><span data-stu-id="648f5-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="648f5-116">Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="648f5-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="648f5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="648f5-117">Requirements</span></span>



| <span data-ttu-id="648f5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="648f5-118">Requirement</span></span> | <span data-ttu-id="648f5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="648f5-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="648f5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="648f5-120">Header</span></span><br/> | <dl> <span data-ttu-id="648f5-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="648f5-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="648f5-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="648f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648f5-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="648f5-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
