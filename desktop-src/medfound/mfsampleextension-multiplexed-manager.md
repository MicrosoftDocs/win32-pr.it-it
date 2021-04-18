---
description: Fornisce un'istanza di IMFMuxStreamSampleManager che viene utilizzata per accedere alla raccolta di campioni dai sottoflussi di un'origine multimediale multifunzione.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: Attributo MFSampleExtension_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b46c277265538ccb2b990ea9d912b9337bcd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310240"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a><span data-ttu-id="e23cb-103">\_ \_ Attributo Gestione multiplex MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="e23cb-103">MFSampleExtension\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="e23cb-104">Fornisce un'istanza di [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) che viene utilizzata per accedere alla raccolta di campioni dai sottoflussi di un'origine multimediale multifunzione.</span><span class="sxs-lookup"><span data-stu-id="e23cb-104">Provides an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) which is used to access the collection of samples from the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="e23cb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e23cb-105">Data type</span></span>

<span data-ttu-id="e23cb-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="e23cb-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="e23cb-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e23cb-107">Remarks</span></span>

<span data-ttu-id="e23cb-108">Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).</span><span class="sxs-lookup"><span data-stu-id="e23cb-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="e23cb-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e23cb-109">Requirements</span></span>



| <span data-ttu-id="e23cb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e23cb-110">Requirement</span></span> | <span data-ttu-id="e23cb-111">Valore</span><span class="sxs-lookup"><span data-stu-id="e23cb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e23cb-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e23cb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e23cb-113">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e23cb-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e23cb-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e23cb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e23cb-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e23cb-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e23cb-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e23cb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23cb-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e23cb-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
