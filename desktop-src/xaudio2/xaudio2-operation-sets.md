---
description: Questa panoramica introduce diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Set di operazioni XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234057"
---
# <a name="xaudio2-operation-sets"></a>Set di operazioni XAudio2

Questa panoramica introduce diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.

Diversi metodi XAudio2 accettano l'argomento *operationt* , che consente di chiamarli come parte di un gruppo posticipato. A un momento specifico, è possibile applicare un intero set di modifiche contemporaneamente chiamando la funzione [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con l'identificatore del set di *operazioni* per il gruppo. L'identificatore è un numero arbitrario. Consente quindi a parti separate del codice client di applicare modifiche atomiche separate al grafo senza conflitti. La procedura consigliata consiste nel fare in modo che il client incrementi un contatore globale ogni volta che è necessario generare un identificatore univoco di un nuovo *operatore* . Un set di modifiche apportate al grafo, applicato in modo atomico, è sicuramente accurato. Ad esempio, le voci vengono avviate sincronizzate.

Se si imposta *Operational* su XAUDIO2 \_ commit \_ Now, la modifica viene applicata immediatamente. Viene applicata nel primo passaggio di elaborazione audio dopo la chiamata al metodo. Se si chiama [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con XAUDIO2 \_ commit \_ All, verranno eseguite le modifiche apportate a tutti i set di operazioni in sospeso, indipendentemente dall'identificatore del set di *operazioni* .

Determinati metodi hanno effetto immediatamente quando vengono chiamati da un callback XAudio2 con un *operatore* di XAudio2 \_ commit \_ Now. Tutti gli altri metodi che accettano un argomento di *operationst* hanno effetto solo sul successivo passaggio di elaborazione dopo che il metodo è stato chiamato (se chiamato con XAUDIO2 \_ commit \_ Now) o dopo la chiamata di [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con lo stesso *operatore*. Per questo motivo, alcune chiamate al metodo potrebbero non essere sempre eseguite nello stesso ordine in cui sono state chiamate.

Tutte le operazioni in sospeso vengono sottoposte a commit in modo atomico quando viene chiamato [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) . Tutti i metodi che vengono chiamati mentre il motore viene arrestato diventano immediatamente effettivi, indipendentemente dal valore di *operationt* fornito. Quando si riavvia il motore, XAudio2 torna alla modalità asincrona.

Gli scenari semplici in cui i set di operazioni sono utili includono gli esempi seguenti.

-   Avvio simultaneo di più voci.
-   Inviando contemporaneamente un buffer a una voce, impostando i parametri vocali e avviando la voce.
-   Creazione di una modifica su larga scala nel grafico, ad esempio la connessione di tutte le voci di origine a una nuova voce submix.

Per un esempio di utilizzo di un set di operazioni, vedere [procedura: raggruppare i metodi audio come set di operazioni](how-to--group-audio-methods-as-an-operation-set.md) .

## <a name="operation-set-methods"></a>Metodi del set di operazioni

È possibile chiamare i metodi seguenti come parte di un set di operazioni.

-   [**IXAudio2SourceVoice::ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice:: sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice:: Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Come descritto in precedenza, il codice client deve infine chiamare la funzione [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) per eseguire le modifiche posticipate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di operazioni](operation-sets.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Raggruppare metodi audio come set di operazioni](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
