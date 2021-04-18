---
description: La proprietà DVDAdm. DefaultAudioLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Proprietà DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304202"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="2e281-103">Proprietà DefaultAudioLCID</span><span class="sxs-lookup"><span data-stu-id="2e281-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="2e281-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2e281-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2e281-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2e281-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2e281-106">La `DVDAdm.DefaultAudioLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="2e281-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="2e281-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e281-107">Return Value</span></span>

<span data-ttu-id="2e281-108">Restituisce un valore intero che rappresenta l'LCID audio predefinito specificato dall'utente come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD.</span><span class="sxs-lookup"><span data-stu-id="2e281-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="2e281-109">Questo valore non è necessariamente uguale al flusso audio predefinito creato nel DVD.</span><span class="sxs-lookup"><span data-stu-id="2e281-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e281-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e281-110">Remarks</span></span>

<span data-ttu-id="2e281-111">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2e281-111">This property is read/write with no default value.</span></span> <span data-ttu-id="2e281-112">Se non viene specificato alcun LCID audio predefinito, l'oggetto MSDVDAdm riprodurrà il flusso audio contrassegnato come flusso predefinito sul disco.</span><span class="sxs-lookup"><span data-stu-id="2e281-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e281-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e281-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e281-114">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="2e281-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



