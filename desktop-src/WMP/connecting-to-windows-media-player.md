---
title: Connessione a Windows Media Player
description: Connessione a Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Plug-in di Windows Media Player, voci del registro di sistema
- plug-in, voci del registro di sistema
- Plug-in di Windows Media Player, connessione
- plug-in, connessione
- plug-in di elaborazione dei segnali digitali, connessione
- Plug-in DSP, connessione
- plug-in di elaborazione dei segnali digitali, voci del registro di sistema
- Plug-in DSP, voci del registro di sistema
- Registro di sistema, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398543"
---
# <a name="connecting-to-windows-media-player"></a>Connessione a Windows Media Player

Windows Media Player si connette automaticamente a plug-in DSP installati e registrati correttamente. I plug-in DSP devono chiamare [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) per creare le voci del registro di sistema necessarie per consentire a Windows Media Player di riconoscere il plug-in e di elencarlo nella scheda **plug-** in della finestra di dialogo Opzioni. Per rimuovere le voci del registro di sistema create da **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin**, il plug-in chiama [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




