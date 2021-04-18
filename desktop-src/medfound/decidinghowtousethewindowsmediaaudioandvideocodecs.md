---
description: Uso degli oggetti codec e DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Uso degli oggetti codec e DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320648"
---
# <a name="using-the-codec-and-dsp-objects"></a>Uso degli oggetti codec e DSP

Esistono diversi modi per usare i codec Windows Media Audio e video e DSP per codificare, decodificare o trasformare il contenuto multimediale digitale. Il Windows Media Audio e il codec video e l'API DSP sono destinati agli utenti che devono configurare manualmente gli oggetti codec e DSP o usarli al di fuori del contesto uno degli SDK di Windows Media, ad esempio Windows Media Format SDK o Media Foundation SDK.

I creatori di contenuti e gli utenti finali possono usare un'ampia gamma di strumenti e applicazioni per codificare il contenuto in flussi Windows Media Audio o Windows Media Video. Windows Media Encoder, ad esempio, è progettato appositamente per semplificare il processo di codifica. Analogamente, Windows Media Player è appositamente progettato per funzionare correttamente con i dati multimediali digitali codificati nei formati Windows Media. Per molte applicazioni, è sufficiente utilizzare Windows Media Encoder SDK o Windows Media Player SDK. In particolare, queste due tecnologie sono valide per gli scenari che assomigliano alla funzionalità degli strumenti che consentono di automatizzare.

Se è necessario un maggiore controllo sul processo di codifica o decodifica, ma si intende comunque utilizzare il formato ASF (Advanced Systems Format) come contenitore per i dati multimediali, Windows Media Format SDK può essere una scelta ottimale. Gli oggetti di Windows Media Format SDK forniscono un framework flessibile per la creazione di file ASF e forniscono supporto incorporato per i codec Windows Media Audio e video.

Il Media Foundation SDK, che è una novità di Windows Vista, semplifica notevolmente la codifica e la decodifica fornendo una pipeline multimediale personalizzabile. È possibile impostare le proprietà dei supporti di input e di output e il caricatore della topologia di Media Foundation configurerà automaticamente i codec necessari e DSP.

Il motivo principale per l'uso diretto degli oggetti codec è l'uso dei codec Windows Media Audio e video all'esterno del contenitore ASF. L'uso degli oggetti codec e DSP fornisce anche un livello di controllo non disponibile con le tecnologie più astratte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



