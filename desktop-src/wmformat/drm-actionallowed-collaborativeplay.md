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
# <a name="drm_actionallowed_collaborativeplay"></a>\_CollaborativePlay ACTIONALLOWED \_ DRM

L' **attributo \_ \_ CollaborativePlay di DRM ActionAllowed** indica se la licenza consente la riproduzione collaborativa del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Per la riproduzione di contenuti protetti come parte di una sessione di collaborazione con servizi peer-to-peer è possibile utilizzare il diritto di collaborazione. Ad esempio, gli utenti di MSN Messenger 2004 possono riprodurre contenuto protetto in una sessione MusicMix. Questo diritto può essere utilizzato solo per fornire un file protetto a una singola sessione alla volta e tutti gli utenti che partecipano alla sessione devono essere online per eseguire il rendering del contenuto.

Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




