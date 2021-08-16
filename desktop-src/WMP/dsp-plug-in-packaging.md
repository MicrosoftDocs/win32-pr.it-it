---
title: Creazione di pacchetti plug-in DSP
description: Creazione di pacchetti plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player plug-in, Media Foundation pipeline
- plug-in, pipeline Media Foundation
- plug-in di elaborazione dei segnali digitali, Media Foundation pipeline
- Plug-in DSP, pipeline Media Foundation
- Media Foundation pipeline
- Windows Media Player plug-in, DirectShow pipeline
- plug-in, pipeline DirectShow
- plug-in di elaborazione dei segnali digitali, DirectShow pipeline
- Plug-in DSP, pipeline DirectShow
- DirectShow pipeline
- plug-in di elaborazione dei segnali digitali, di base
- plug-in DSP, di base
- Windows Media Player plug-in, DSP di base
- plug-in, DSP di base
- plug-in DSP di base
- Windows Media Player plug-in, DSP dual mode
- plug-in, DSP dual mode
- plug-in di elaborazione del segnale digitale, modalità doppia
- Plug-in DSP, modalità doppia
- plug-in DSP dual-mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bd87e1729b4d8759f3b9f1d7d4d7993660512d49c34ea9bf9aa34802b69cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749506"
---
# <a name="dsp-plug-in-packaging"></a>Creazione di pacchetti plug-in DSP

Windows Media Player esegue il rendering di audio e video usando una delle pipeline seguenti.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP e versioni precedenti, Player usa DirectShow. In Windows Vista, il lettore a volte usa DirectShow e a volte usa Media Foundation.

Un plug-in DSP progettato per l'esecuzione nella pipeline DirectShow è denominato *plug-in DSP di base.* Un plug-in DSP di base funge da oggetto multimediale DirectX (DMO). Un plug-in DSP di base può essere eseguito in modo nativo nella pipeline di DirectShow e può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation.

Un plug-in DSP progettato per l'esecuzione in modalità nativa (nessun wrapper necessario) nelle pipeline DirectShow e Media Foundation è denominato *plug-in DSP* in modalità doppia. Un plug-in DSP dual mode può fungere da DMO o da Media Foundation Transform (MFT).

Un plug-in DSP è un oggetto COM in pacchetto come file di .dll autoregistrazione. Le interfacce implementate dal plug-in variano a seconda che il plug-in sia progettato come plug-in DSP di base o come plug-in DSP dual-mode. Per informazioni dettagliate sulle interfacce che i plug-in DSP devono implementare, vedere [Interfacce necessarie.](required-interfaces.md)

Un plug-in DSP eseguito nella pipeline di Media Foundation (in modo nativo o di cui è stato eseguito il wrapping) deve registrare il modello di threading come "Both". Per informazioni dettagliate sulle sottochiavi del Registro di sistema e sulle voci associate ai plug-in DSP, vedere [Registrazione dei plug-in DSP.](registering-dsp-plug-ins.md)

Un plug-in DSP che implementa interfacce personalizzate ed esecuzioni nella pipeline di Media Foundation (in modo nativo o di cui è stato eseguito il wrapping) deve essere associato a un file .dll proxy-stub in grado di effettuare il marshalling delle interfacce personalizzate tra i limiti del processo. Per informazioni sul componente proxy-stub, vedere Aggiornamento di [plug-in DSP](updating-existing-dsp-plug-ins.md) esistenti e Aggiornamenti della Creazione guidata [plug-in DSP per Windows Media Player 11.](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)

Gli oggetti plug-in DSP non devono essere creati come singleton. Windows Media Player essere in grado di creare più istanze separate di un particolare plug-in DSP.

I plug-in DSP eseguiti nel Windows Vista Protected Media Path (PMP) devono essere firmati. Per altre informazioni, vedere [Firma del codice per i componenti multimediali protetti in Windows Vista.](/windows-hardware/test/hlk/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 