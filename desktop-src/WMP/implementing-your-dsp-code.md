---
title: Implementazione del codice DSP
description: Implementazione del codice DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Windows Media Player plug-in, digital signal processing (DSP)
- plug-in, elaborazione del segnale digitale (DSP)
- plug-in di elaborazione del segnale digitale, implementazione di codice
- plug-in DSP, implementazione di codice
- plug-in di elaborazione del segnale digitale, modifica del codice di esempio
- plug-in DSP, modifica del codice di esempio
- plug-in DSP audio, implementazione di codice
- plug-in DSP video, implementazione di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8504a44b9f3e980be612569e9b7cbe06081d0bfe704a5932e44eef789127687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135564"
---
# <a name="implementing-your-dsp-code"></a>Implementazione del codice DSP

Dopo aver compilato il plug-in DSP di esempio, è possibile modificare il codice per creare un plug-in DSP Windows Media Player personalizzato. I metodi che è possibile modificare e che è possibile lasciare così come sono dipendono dai fattori seguenti:

-   Numero di proprietà che si desidera consentire all'utente di modificare. È certamente necessario modificare l'implementazione predefinita della pagina delle proprietà in base alle proprie esigenze e potrebbe essere necessario aggiungere altre proprietà.
-   Indica se il plug-in DSP deve allocare le risorse di streaming. Il plug-in potrebbe richiedere buffer aggiuntivi.
-   Indica se il plug-in DSP audio deve continuare a determinare l'output dei dati dopo Windows Media Player ha interrotto l'inserimento di dati nel buffer di input.

Le sezioni seguenti usano il codice di esempio del plug-in DSP generato dalla Windows Media Player guidata plug-in per illustrare concetti importanti. Potrebbe essere utile aprire prima Microsoft Visual Studio e generare il codice di esempio in modo da poter fare riferimento ad esso durante la lettura di questa sezione. Per informazioni dettagliate su come usare la Windows Media Player guidata plug-in, vedere Compilazione di [un plug-in DSP.](building-a-dsp-plug-in.md)



| Sezione                                                                    | Descrizione                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementazione di un plug-in DSP audio](implementing-an-audio-dsp-plug-in.md) | Illustra le informazioni necessarie per creare un plug-in DSP audio personalizzato in base all'esempio generato dalla procedura guidata. |
| [Implementazione di un plug-in DSP video](implementing-a-video-dsp-plug-in.md)   | Illustra le informazioni necessarie per creare un plug-in DSP video personalizzato in base all'esempio generato dalla procedura guidata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




