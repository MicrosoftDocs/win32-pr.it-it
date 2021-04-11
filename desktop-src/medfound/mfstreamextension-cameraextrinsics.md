---
description: Contiene la fotocamera estrinseca per il flusso.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Attributo MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130518"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a><span data-ttu-id="29256-103">\_Attributo CameraExtrinsics di MFStreamExtension</span><span class="sxs-lookup"><span data-stu-id="29256-103">MFStreamExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="29256-104">Contiene la fotocamera estrinseca per il flusso.</span><span class="sxs-lookup"><span data-stu-id="29256-104">Contains the camera extrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="29256-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="29256-105">Data type</span></span>

<span data-ttu-id="29256-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="29256-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="29256-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="29256-107">Get/set</span></span>

<span data-ttu-id="29256-108">Per ottenere questo attributo, chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="29256-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="29256-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="29256-109">Remarks</span></span>

<span data-ttu-id="29256-110">Il valore dell'attributo è un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="29256-110">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="29256-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29256-111">Requirements</span></span>



| <span data-ttu-id="29256-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="29256-112">Requirement</span></span> | <span data-ttu-id="29256-113">Valore</span><span class="sxs-lookup"><span data-stu-id="29256-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29256-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29256-114">Minimum supported client</span></span><br/> | <span data-ttu-id="29256-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="29256-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29256-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29256-116">Minimum supported server</span></span><br/> | <span data-ttu-id="29256-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="29256-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="29256-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29256-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="29256-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="29256-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




