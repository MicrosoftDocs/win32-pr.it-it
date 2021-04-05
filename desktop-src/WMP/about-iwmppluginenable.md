---
title: Informazioni su IWMPPluginEnable
description: Informazioni su IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IWMPPluginEnable
- plug-in, interfaccia IWMPPluginEnable
- plug-in per l'elaborazione di segnali digitali, interfaccia IWMPPluginEnable
- Plug-in DSP, interfaccia IWMPPluginEnable
- Interfaccia IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955195"
---
# <a name="about-iwmppluginenable"></a>Informazioni su IWMPPluginEnable

L'interfaccia **IWMPPluginEnable** è necessaria per i plug-in di Windows Media Player DSP. **IWMPPluginEnable** contiene due metodi che archiviano se Windows Media Player ha abilitato il plug-in DSP. Windows Media Player chiama **IWMPPluginEnable:: seenable** quando crea un'istanza del plug-in DSP, passando un valore **true** se il plug-in è stato abilitato o **false** in caso contrario.

È possibile che i plug-in DSP rimangano caricati anche quando l'utente sceglie di disabilitarli. Quando è disabilitato, un plug-in deve copiare i dati dal buffer di input nel buffer di output, eseguendo solo l'elaborazione della conversione del formato, se applicabile.

Windows Media Player chiama inoltre questo metodo prima di rilasciare un'istanza del plug-in DSP. Questa operazione è utile per consentire ai client del plug-in di verificare se il plug-in è attualmente abilitato. Un plug-in dell'interfaccia utente, ad esempio, potrebbe modificare l'aspetto dei controlli per avvisare l'utente che il plug-in DSP non è connesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce obbligatorie**](required-interfaces.md)
</dt> </dl>

 

 




