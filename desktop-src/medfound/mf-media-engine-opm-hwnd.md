---
description: Specifica una finestra per il motore multimediale per applicare le protezioni di output Protection Manager (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Attributo MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968881"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="c3437-103">\_ \_ \_ \_ Attributo HWND hWnd del motore multimediale MF</span><span class="sxs-lookup"><span data-stu-id="c3437-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="c3437-104">Specifica una finestra per il motore multimediale per applicare le protezioni di [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="c3437-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3437-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c3437-105">Data type</span></span>

<span data-ttu-id="c3437-106">**HWND** archiviato come **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3437-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3437-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3437-107">Remarks</span></span>

<span data-ttu-id="c3437-108">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3437-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="c3437-109">Per abilitare le protezioni di OPM per la riproduzione video, l'applicazione deve eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3437-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="c3437-110">Impostare l'attributo HWND per la [ \_ \_ \_ riproduzione \_ del motore multimediale MF](mf-media-engine-playback-hwnd.md) quando si crea il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3437-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="c3437-111">Impostare l' \_ \_ attributo HWND hWnd del motore multimediale MF \_ quando si \_ Crea il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3437-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="c3437-112">Chiamare [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) in qualsiasi momento dopo aver creato il motore multimediale, ma prima di visualizzare il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="c3437-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3437-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3437-113">Requirements</span></span>



| <span data-ttu-id="c3437-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3437-114">Requirement</span></span> | <span data-ttu-id="c3437-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c3437-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3437-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3437-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3437-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c3437-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="c3437-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3437-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3437-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3437-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="c3437-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3437-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3437-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3437-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3437-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3437-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3437-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3437-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3437-124">Attributi del motore multimediale</span><span class="sxs-lookup"><span data-stu-id="c3437-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




