---
description: Supporto di VMR per l'accelerazione video DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Supporto di VMR per l'accelerazione video DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753810"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Supporto di VMR per l'accelerazione video DirectX

L'accelerazione video DirectX è un'API (Application Programming Interface) e un'interfaccia DDI (Device Driver Interface) corrispondente per l'accelerazione hardware dell'elaborazione della decodifica video digitale, con supporto della fusione alfa per tali scopi come supporto per le immagini di DVD. DirectX VA documentato nel DDK di Windows. L'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , che fornisce l'accesso in modalità utente alla funzionalità DirectX va in un dispositivo hardware, è documentata in questo SDK.

VMR supporta [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)e la relativa implementazione è identica a quella del vecchio mixer sovrapposto, ad eccezione di una differenza importante. Il mixer di sovrimpressione ha garantito che l'output venga sottoposto a rendering in una superficie sovrapposta, mentre VMR può inviare l'output per un'ulteriore elaborazione, ad esempio un'operazione 3D, oppure inviare l'output a una superficie Offscreen che viene quindi blitted alla superficie primaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'accelerazione video DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



