---
description: Imposta una finestra per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332664"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="7308e-103">MFPKEY \_ http \_ ByteStream \_ \_ proprietà finestra Urlmon</span><span class="sxs-lookup"><span data-stu-id="7308e-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="7308e-104">Imposta una finestra per il flusso di byte HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7308e-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="7308e-105">La finestra viene utilizzata per presentare informazioni nell'interfaccia utente durante un'operazione di associazione.</span><span class="sxs-lookup"><span data-stu-id="7308e-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="7308e-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7308e-106">Data type</span></span>

<span data-ttu-id="7308e-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="7308e-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7308e-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="7308e-108">PROPVARIANT member</span></span>

<span data-ttu-id="7308e-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="7308e-109">**IUnknown\***</span></span>

<span data-ttu-id="7308e-110">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="7308e-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="7308e-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="7308e-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="7308e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7308e-112">Remarks</span></span>

<span data-ttu-id="7308e-113">Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7308e-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="7308e-114">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="7308e-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="7308e-115">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="7308e-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="7308e-116">Il valore di questa proprietà è un puntatore all'interfaccia **IWindowForBindingUI** .</span><span class="sxs-lookup"><span data-stu-id="7308e-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="7308e-117">Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="7308e-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7308e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7308e-118">Requirements</span></span>



| <span data-ttu-id="7308e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7308e-119">Requirement</span></span> | <span data-ttu-id="7308e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7308e-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7308e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7308e-121">Header</span></span><br/> | <dl> <span data-ttu-id="7308e-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7308e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7308e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7308e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7308e-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7308e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
