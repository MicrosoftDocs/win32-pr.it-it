---
title: Interfacce video Direct3D
description: Questo argomento elenca le interfacce video Direct3D disponibili in Direct3D 9Ex e supportate in Windows 7 e versioni successive dei sistemi operativi client Windows e in Windows Server 2008 R2 e versioni successive dei sistemi operativi Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473334"
---
# <a name="direct3d-video-interfaces"></a>Interfacce video Direct3D

Questo argomento elenca le interfacce video Direct3D disponibili in Direct3D 9Ex e supportate in Windows 7 e versioni successive dei sistemi operativi client Windows e in Windows Server 2008 R2 e versioni successive dei sistemi operativi Windows Server. È possibile utilizzare queste interfacce e i relativi metodi per ottenere le funzionalità di protezione del contenuto video del driver grafico e le funzionalità hardware sovrapposte di un dispositivo Direct3D. È anche possibile usare queste interfacce e i relativi metodi per proteggere il contenuto video. Queste interfacce e i relativi metodi sono definiti in d3d9. h e descritti nella sezione [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .



| Interfaccia                                                                                                                                                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Esegue una query sulle funzionalità hardware sovrapposte di un dispositivo Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Fornisce un canale di comunicazione con il driver di grafica o il runtime Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Rappresenta una sessione di crittografia utilizzata per accedere a una superficie protetta.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Consente a un'applicazione di utilizzare i servizi di crittografia e protezione del contenuto implementati da un driver di grafica.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

