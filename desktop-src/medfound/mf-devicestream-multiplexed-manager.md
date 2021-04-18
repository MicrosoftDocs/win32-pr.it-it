---
description: Fornisce un'istanza di IMFMuxStreamAttributesManager che gestisce gli IMFAttributes che descrivono i sottoflussi di un'origine multimediale con multiplexing.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Attributo MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309573"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="28308-103">\_Attributo di \_ Gestione multiplex MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="28308-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="28308-104">Fornisce un'istanza di [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) che gestisce gli [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) che descrivono i sottoflussi di un'origine multimediale con multiplexing.</span><span class="sxs-lookup"><span data-stu-id="28308-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="28308-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="28308-105">Data type</span></span>

<span data-ttu-id="28308-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="28308-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="28308-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="28308-107">Remarks</span></span>

<span data-ttu-id="28308-108">Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per determinare se l'origine multimediale fornisce flussi multiplexati e, in caso affermativo, ottenere un'istanza di [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span><span class="sxs-lookup"><span data-stu-id="28308-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="28308-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28308-109">Requirements</span></span>



| <span data-ttu-id="28308-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="28308-110">Requirement</span></span> | <span data-ttu-id="28308-111">Valore</span><span class="sxs-lookup"><span data-stu-id="28308-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28308-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28308-112">Minimum supported client</span></span><br/> | <span data-ttu-id="28308-113">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="28308-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28308-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28308-114">Minimum supported server</span></span><br/> | <span data-ttu-id="28308-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="28308-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="28308-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28308-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="28308-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28308-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
