---
description: Questa panoramica presenta diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Set di operazioni XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089411"
---
# <a name="xaudio2-operation-sets"></a>Set di operazioni XAudio2

Questa panoramica presenta diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.

Diversi metodi XAudio2 accettano *l'argomento OperationSet,* che consente di chiamarli come parte di un gruppo posticipato. In un momento specifico, è possibile applicare contemporaneamente un intero set di modifiche chiamando la funzione [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con l'identificatore *OperationSet* per il gruppo. L'identificatore è un numero arbitrario. Consente quindi a parti separate del codice client di applicare modifiche atomiche separate al grafo senza conflitti. È consigliabile che il client incrementi un contatore globale ogni volta che deve generare un identificatore *OperationSet* univoco e nuovo. È garantito che un set di modifiche al grafo, applicato in modo atomico, sia accurato per il campione. Ad esempio, le voci verranno avviate in modo sincronizzato.

Se si imposta *OperationSet* su XAUDIO2 \_ COMMIT \_ NOW, la modifica viene applicata immediatamente. Ha effetto nel primo passaggio di elaborazione audio dopo la chiamata al metodo . Se si chiama [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con XAUDIO2 COMMIT ALL, vengono eseguite le modifiche a tutti i set di operazioni in sospeso, indipendentemente dal \_ relativo identificatore \_ *OperationSet.*

Alcuni metodi hanno effetto immediato quando vengono chiamati da un callback XAudio2 con *OperationSet* di XAUDIO2 \_ COMMIT \_ NOW. Tutti gli altri metodi che accettano un argomento *OperationSet* hanno effetto solo al successivo passaggio di elaborazione dopo la chiamata del metodo (se chiamato con XAUDIO2 COMMIT NOW) o dopo che \_ \_ [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) viene chiamato con lo stesso *OperationSet*. Per questo problema, alcune chiamate al metodo potrebbero non essere sempre effettuate nello stesso ordine in cui sono state chiamate.

Il commit di tutte le operazioni in sospeso viene eseguito in modo atomico quando viene chiamato [**IXAudio2::StopEngine.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) Tutti i metodi chiamati mentre il motore viene arrestato hanno effetto immediato, indipendentemente dal *valore operationSet* fornito. Quando si riavvia il motore, XAudio2 torna alla modalità asincrona.

Gli scenari semplici in cui i set di operazioni sono utili includono gli esempi seguenti.

-   Avvio simultaneo di più voci.
-   Invio simultaneo di un buffer a una voce, impostazione dei parametri vocali e avvio della voce.
-   Modifica su larga scala del grafico, ad esempio la connessione di tutte le voci di origine a una nuova voce submix.

Per [un esempio d'uso di un](how-to--group-audio-methods-as-an-operation-set.md) set di operazioni, vedere Procedura: Raggruppare metodi audio come set di operazioni.

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
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice::Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Come descritto in precedenza, il codice client deve chiamare la funzione [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) per eseguire le modifiche posticipate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di operazioni](operation-sets.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Raggruppare metodi audio come set di operazioni](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
