---
title: Per impostare le impostazioni di input
description: Per impostare le impostazioni di input
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), impostazioni di input
- ASF (formato avanzato dei sistemi), impostazioni di input
- profili, impostazioni di input
- codec, impostazioni di input
- flussi, impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956199"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="7f69a-108">Per impostare le impostazioni di input</span><span class="sxs-lookup"><span data-stu-id="7f69a-108">To Set Input Settings</span></span>

<span data-ttu-id="7f69a-109">Le proprietà di base dei supporti di input e del flusso sono definite dalla struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="7f69a-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="7f69a-110">Per i formati di input, le informazioni sul tipo di supporto sono impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f69a-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="7f69a-111">Per i formati di flusso, le informazioni sul tipo di supporto sono impostate nel profilo assegnato al writer.</span><span class="sxs-lookup"><span data-stu-id="7f69a-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="7f69a-112">Alcune proprietà sono indipendenti dal tipo di supporto e devono essere impostate per un input prima che inizi la scrittura.</span><span class="sxs-lookup"><span data-stu-id="7f69a-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="7f69a-113">Queste proprietà sono funzionalità di codec e writer indipendenti dal tipo di flusso e devono essere impostate dopo l'assegnazione del profilo nel writer, ma prima dell'inizio della scrittura.</span><span class="sxs-lookup"><span data-stu-id="7f69a-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="7f69a-114">Per l'impostazione di un'impostazione di input è richiesta una chiamata a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="7f69a-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="7f69a-115">È anche possibile controllare il valore corrente di un'impostazione con una chiamata a [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span><span class="sxs-lookup"><span data-stu-id="7f69a-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f69a-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f69a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f69a-117">**Per utilizzare profili con il writer**</span><span class="sxs-lookup"><span data-stu-id="7f69a-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="7f69a-118">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="7f69a-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="7f69a-119">**Scrittura di flussi di immagini**</span><span class="sxs-lookup"><span data-stu-id="7f69a-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




