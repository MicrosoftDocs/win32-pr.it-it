---
description: Supporto vmr per l'accelerazione video DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Supporto vmr per l'accelerazione video DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696731"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Supporto vmr per l'accelerazione video DirectX

L'accelerazione video DirectX è un'API (Application Programming Interface) e un'interfaccia DDI (Device Driver Interface) corrispondente per l'accelerazione hardware dell'elaborazione della decodifica video digitale, con supporto della fusione alfa per scopi quali il supporto delle immagini secondarie DVD. DirectX VA è documentato nella Windows DDK. [**L'interfaccia IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) che fornisce l'accesso in modalità utente alla funzionalità DirectX VA in un dispositivo hardware, è documentata in questo SDK.

La macchina virtuale supporta [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)e la relativa implementazione è identica alla versione precedente di Overlay Mixer ad eccezione di una differenza importante. L'Mixer Overlay garantisce che il rendering dell'output venga eseguito in una superficie di sovrapposizione, mentre la macchina virtuale può inviare l'output per un'ulteriore elaborazione, ad esempio un'operazione 3D, oppure può inviare l'output a una superficie fuori schermo che viene quindi sottoposta a blitt alla superficie primaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'accelerazione video DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



