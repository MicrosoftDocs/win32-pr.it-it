---
title: DRM_ActionAllowed_CollaborativePlay
description: L' \_ \_ attributo COLLABORATIVEPLAY di DRM ActionAllowed indica se la licenza consente la riproduzione collaborativa del contenuto.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398618"
---
# <a name="drm_actionallowed_collaborativeplay"></a><span data-ttu-id="a678d-104">\_CollaborativePlay ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="a678d-104">DRM\_ActionAllowed\_CollaborativePlay</span></span>

<span data-ttu-id="a678d-105">L' **attributo \_ \_ CollaborativePlay di DRM ActionAllowed** indica se la licenza consente la riproduzione collaborativa del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a678d-105">The **DRM\_ActionAllowed\_CollaborativePlay** attribute indicates whether the license allows the content to be played collaboratively.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a678d-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a678d-106">Global Constant</span></span>

<span data-ttu-id="a678d-107">g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="a678d-107">g\_wszWMDRM\_ActionAllowed\_CollaborativePlay</span></span>

## <a name="data-type"></a><span data-ttu-id="a678d-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a678d-108">Data Type</span></span>

<span data-ttu-id="a678d-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a678d-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="a678d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a678d-110">Remarks</span></span>

<span data-ttu-id="a678d-111">Per la riproduzione di contenuti protetti come parte di una sessione di collaborazione con servizi peer-to-peer è possibile utilizzare il diritto di collaborazione.</span><span class="sxs-lookup"><span data-stu-id="a678d-111">The collaborative play right applies to playing protected content as part of a collaborative session using peer-to-peer services.</span></span> <span data-ttu-id="a678d-112">Ad esempio, gli utenti di MSN Messenger 2004 possono riprodurre contenuto protetto in una sessione MusicMix.</span><span class="sxs-lookup"><span data-stu-id="a678d-112">For example, users of MSN Messenger 2004 can play protected content in a MusicMix session.</span></span> <span data-ttu-id="a678d-113">Questo diritto può essere utilizzato solo per fornire un file protetto a una singola sessione alla volta e tutti gli utenti che partecipano alla sessione devono essere online per eseguire il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a678d-113">This right can only be used to contribute a protected file to a single session at one time, and all users participating in the session must be online to render the content.</span></span>

<span data-ttu-id="a678d-114">Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="a678d-114">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="a678d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a678d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a678d-116">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="a678d-116">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




