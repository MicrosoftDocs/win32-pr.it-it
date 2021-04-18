---
title: Implementazione del codice DSP
description: Implementazione del codice DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Plug-in di Windows Media Player, elaborazione dei segnali digitali (DSP)
- plug-in, elaborazione di segnali digitali (DSP)
- plug-in di elaborazione dei segnali digitali, implementazione del codice
- Plug-in DSP, implementazione del codice
- plug-in di elaborazione dei segnali digitali, modifica del codice di esempio
- Plug-in DSP, modifica del codice di esempio
- plug-in DSP audio, implementazione del codice
- plug-in di video DSP, implementazione del codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9e17dad39a4ba0ebe79e31d9f3eead843d7f81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298392"
---
# <a name="implementing-your-dsp-code"></a>Implementazione del codice DSP

Dopo aver compilato il plug-in DSP di esempio, è possibile modificare il codice per creare il proprio plug-in Windows Media Player DSP. I metodi modificati e che è possibile lasciare come dipendono dai fattori seguenti:

-   Il numero di proprietà che si desidera consentire all'utente di modificare. È certamente opportuno modificare l'implementazione della pagina delle proprietà predefinita in base alle esigenze e potrebbe essere necessario aggiungere ulteriori proprietà.
-   Se il plug-in DSP deve allocare risorse di streaming. Il plug-in potrebbe richiedere buffer aggiuntivi.
-   Se il plug-in DSP audio deve continuare a restituire i dati dopo che Windows Media Player ha interrotto l'immissione dei dati nel buffer di input.

Nelle sezioni seguenti viene utilizzato il codice di esempio del plug-in DSP generato dalla procedura guidata plug-in di Windows Media Player per illustrare concetti importanti. Potrebbe essere utile aprire Microsoft Visual Studio e generare prima il codice di esempio in modo che sia possibile farvi riferimento durante la lettura di questa sezione. Per informazioni dettagliate sull'utilizzo della creazione guidata plug-in di Windows Media Player, vedere la pagina relativa alla [creazione di un plug-in DSP](building-a-dsp-plug-in.md).



| Sezione                                                                    | Descrizione                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementazione di un plug-in DSP audio](implementing-an-audio-dsp-plug-in.md) | Vengono illustrate le informazioni necessarie per creare un plug-in DSP audio personalizzato basato sull'esempio generato dalla procedura guidata. |
| [Implementazione di un plug-in video DSP](implementing-a-video-dsp-plug-in.md)   | Illustra le informazioni necessarie per creare il plug-in video DSP personalizzato in base all'esempio generato dalla procedura guidata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




