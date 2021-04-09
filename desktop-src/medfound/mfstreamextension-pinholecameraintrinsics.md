---
description: Contiene le funzioni intrinseche della fotocamera pinhole per il flusso.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: Attributo MFStreamExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967126"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="53767-103">\_Attributo PinholeCameraIntrinsics di MFStreamExtension</span><span class="sxs-lookup"><span data-stu-id="53767-103">MFStreamExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="53767-104">Contiene le funzioni intrinseche della fotocamera pinhole per il flusso.</span><span class="sxs-lookup"><span data-stu-id="53767-104">Contains the pinhole camera intrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="53767-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="53767-105">Data type</span></span>

<span data-ttu-id="53767-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="53767-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="53767-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="53767-107">Get/set</span></span>

<span data-ttu-id="53767-108">Per ottenere questo attributo, chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="53767-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="53767-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="53767-109">Remarks</span></span>

<span data-ttu-id="53767-110">Il valore dell'attributo è un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="53767-110">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="53767-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53767-111">Requirements</span></span>



| <span data-ttu-id="53767-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="53767-112">Requirement</span></span> | <span data-ttu-id="53767-113">Valore</span><span class="sxs-lookup"><span data-stu-id="53767-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53767-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53767-114">Minimum supported client</span></span><br/> | <span data-ttu-id="53767-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="53767-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53767-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53767-116">Minimum supported server</span></span><br/> | <span data-ttu-id="53767-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="53767-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="53767-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53767-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="53767-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53767-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




