---
description: Ottiene un oggetto di tipo IMFCollection contenente gli oggetti IMFSample che contengono le unità di astrazione del livello di rete (NALUs) e le informazioni sul miglioramento supplementare (SEI) che vengono trasmesse da un decodificatore.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Attributo MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310241"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="0d4ce-103">\_Attributo ForwardedDecodeUnits di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="0d4ce-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="0d4ce-104">Ottiene un oggetto di tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenente gli oggetti [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che contengono le unità di astrazione del livello di rete (NALUs) e le informazioni sul miglioramento supplementare (sei) che vengono trasmesse da un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d4ce-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0d4ce-105">Data type</span></span>

<span data-ttu-id="0d4ce-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="0d4ce-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4ce-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d4ce-107">Remarks</span></span>

<span data-ttu-id="0d4ce-108">La raccolta contiene tutte le unità NALU/SEI personalizzate a partire dal fotogramma precedente con i byte di prevenzione dell'emulazione rimossi.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4ce-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d4ce-109">Requirements</span></span>



| <span data-ttu-id="0d4ce-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4ce-110">Requirement</span></span> | <span data-ttu-id="0d4ce-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4ce-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4ce-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4ce-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4ce-113">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d4ce-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d4ce-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4ce-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4ce-115">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0d4ce-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d4ce-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d4ce-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4ce-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4ce-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




