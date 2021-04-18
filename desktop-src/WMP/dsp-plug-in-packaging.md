---
title: Creazione del pacchetto di plug-in DSP
description: Creazione del pacchetto di plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-in di Windows Media Player, pipeline Media Foundation
- plug-in, pipeline di Media Foundation
- plug-in per l'elaborazione di segnali digitali, pipeline di Media Foundation
- Plug-in DSP, pipeline di Media Foundation
- Pipeline Media Foundation
- Plug-in di Windows Media Player, pipeline DirectShow
- plug-in, pipeline DirectShow
- plug-in di elaborazione dei segnali digitali, pipeline DirectShow
- Plug-in DSP, pipeline DirectShow
- Pipeline DirectShow
- plug-in per l'elaborazione di segnali digitali, di base
- Plug-in DSP, di base
- Plug-in di Windows Media Player, DSP Basic
- plug-in, DSP di base
- plug-in DSP di base
- Plug-in di Windows Media Player, DSP Dual Mode
- plug-in, DSP Dual Mode
- plug-in di elaborazione dei segnali digitali, Dual Mode
- Plug-in DSP, modalità duale
- plug-in DSP a doppia modalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300002"
---
# <a name="dsp-plug-in-packaging"></a>Creazione del pacchetto di plug-in DSP

Windows Media Player esegue il rendering di audio e video utilizzando una delle seguenti pipeline.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP e versioni precedenti, il lettore utilizza DirectShow. In Windows Vista, il lettore talvolta utilizza DirectShow e talvolta utilizza Media Foundation.

Un plug-in DSP progettato per essere eseguito nella pipeline DirectShow è denominato *plug-in DSP di base*. Un plug-in DSP di base funge da oggetto DMO (DirectX Media Object). Un plug-in DSP di base può essere eseguito in modalità nativa nella pipeline DirectShow e può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation.

Un plug-in DSP progettato per l'esecuzione a livello nativo (senza wrapper necessario) sia nella pipeline DirectShow che in quella Media Foundation viene definito *plug-in DSP a doppia modalità*. Un plug-in DSP in modalità duale può fungere da DMO o come trasformazione Media Foundation (MFT).

Un plug-in DSP è un oggetto COM confezionato come file con estensione dll autoregistrato. Le interfacce implementate dal plug-in variano a seconda che il plug-in sia stato progettato come plug-in DSP di base o come plug-in DSP a doppia modalità. Per informazioni dettagliate sulle interfacce che devono essere implementate dai plug-in DSP, vedere [interfacce obbligatorie](required-interfaces.md).

Un plug-in DSP eseguito nella pipeline Media Foundation (in modo nativo o di cui è stato eseguito il wrapper) deve registrare il modello di threading come "both". Per informazioni dettagliate sulle sottochiavi del registro di sistema e le voci associate ai plug-in DSP, vedere [registrazione dei plug-in DSP](registering-dsp-plug-ins.md).

Un plug-in DSP che implementa interfacce personalizzate e viene eseguito nella pipeline Media Foundation (in modalità nativa o a capo) deve essere associato a un file con estensione dll dello stub proxy in grado di effettuare il marshalling delle interfacce personalizzate tra i limiti dei processi. Per informazioni sul componente stub-proxy, vedere [aggiornamento dei plug-in DSP esistenti](updating-existing-dsp-plug-ins.md) e [aggiornamenti alla procedura guidata plug-in dsp per Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Gli oggetti plug-in DSP non devono essere creati come singleton. Windows Media Player deve essere in grado di creare più istanze separate di un plug-in DSP specifico.

I plug-in DSP eseguiti in Windows Vista Protected Media Path (PMP) devono essere firmati. Per ulteriori informazioni, vedere [la pagina relativa alla firma del codice per i componenti multimediali protetti in Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 