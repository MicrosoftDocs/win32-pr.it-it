---
description: Fornisce un'istanza di IMFMuxStreamMediaTypeManager che può essere usata per ottenere i tipi di supporto dei flussi sottoflussi di un'origine multimediale con multiplexing, nonché per controllare la combinazione di sottoflussi multiplexati dall'origine.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Attributo MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234488"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a><span data-ttu-id="a952a-103">\_Attributo di \_ Gestione multiplex MF MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="a952a-103">MF\_MEDIATYPE\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="a952a-104">Fornisce un'istanza di [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) che può essere usata per ottenere i tipi di supporto dei flussi sottoflussi di un'origine multimediale con multiplexing, nonché per controllare la combinazione di sottoflussi multiplexati dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a952a-104">Provides an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) which can be used to get the media types of the substreams of a multiplexed media source as well as control the combination of substreams that are multiplexed by the source.</span></span>

## <a name="data-type"></a><span data-ttu-id="a952a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a952a-105">Data type</span></span>

<span data-ttu-id="a952a-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="a952a-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="a952a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a952a-107">Remarks</span></span>

<span data-ttu-id="a952a-108">Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span><span class="sxs-lookup"><span data-stu-id="a952a-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="a952a-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a952a-109">Requirements</span></span>



| <span data-ttu-id="a952a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a952a-110">Requirement</span></span> | <span data-ttu-id="a952a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a952a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a952a-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a952a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a952a-113">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="a952a-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a952a-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a952a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a952a-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a952a-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a952a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a952a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a952a-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a952a-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
