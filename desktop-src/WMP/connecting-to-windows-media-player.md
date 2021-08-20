---
title: Connessione a Windows Media Player
description: Connessione a Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Windows Media Player plug-in, voci del Registro di sistema
- plug-in, voci del Registro di sistema
- Windows Media Player plug-in, connessione
- plug-in, connessione
- plug-in di elaborazione del segnale digitale, connessione
- plug-in DSP, connessione
- plug-in di elaborazione del segnale digitale, voci del Registro di sistema
- Plug-in DSP, voci del Registro di sistema
- registro, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d266f1715147d3c7631909e8e23e3e7b1f786337c998d188968a96f6c26b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997631"
---
# <a name="connecting-to-windows-media-player"></a>Connessione a Windows Media Player

Windows Media Player si connette automaticamente ai plug-in DSP installati e registrati correttamente. I plug-in DSP devono chiamare [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) per creare le voci del Registro di sistema necessarie per consentire a Windows Media Player di riconoscere il plug-in ed elencarlo nella **scheda Plug-in della** finestra di dialogo Opzioni. Per rimuovere le voci del Registro di sistema create da **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, il plug-in chiama [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




