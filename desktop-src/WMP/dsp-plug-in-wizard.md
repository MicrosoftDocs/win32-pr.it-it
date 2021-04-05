---
title: Procedura guidata plug-in DSP
description: Procedura guidata plug-in DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-in di Windows Media Player, creazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in di elaborazione dei segnali digitali, creazione guidata plug-in
- Plug-in DSP, creazione guidata plug-in
- procedura guidata plug-in
- Visual Studio, creazione guidata plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515694"
---
# <a name="dsp-plug-in-wizard"></a>Procedura guidata plug-in DSP

Windows Media Player SDK fornisce una procedura guidata plug-in che è possibile aggiungere a Visual Studio. La procedura guidata può generare codice di esempio per un'ampia gamma di plug-in, inclusi i seguenti tipi di plug-in DSP:

-   Plug-in DSP audio
-   Plug-in DSP audio (modalità duale)
-   Plug-in DSP video
-   Plug-in video DSP (modalità duale)

Ognuno dei due plug-in di esempio di base, DSP audio e video DSP, funziona come un oggetto DMO (DirectX Media Object). Ovvero ogni plug-in di esempio implementa l'interfaccia **IMediaObject** . Ognuno dei due plug-in di esempio dual mode può fungere da DMO o come trasformazione Media Foundation (MFT). Ovvero, ogni plug-in di esempio Dual-Mode implementa sia l'interfaccia **IMediaObject** che l'interfaccia **IMFTransform** .

È possibile compilare, collegare, registrare e testare il codice del plug-in di esempio. È quindi possibile modificare il codice di esempio generato per creare il plug-in DSP personalizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




