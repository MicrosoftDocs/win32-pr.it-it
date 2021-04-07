---
description: Controllo qualità predefinito
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Controllo qualità predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048881"
---
# <a name="default-quality-control"></a>Controllo qualità predefinito

Le [classi base di DirectShow](directshow-base-classes.md) implementano alcuni comportamenti predefiniti per il controllo della qualità dei video.

I messaggi qualitativi iniziano dal renderer. La classe base per i renderer video è [**CBaseVideoRenderer**](cbasevideorenderer.md), che presenta il comportamento seguente:

1.  Quando il renderer video riceve un campione, confronta il timestamp dell'esempio con l'ora di riferimento corrente.
2.  Il renderer video genera un messaggio di qualità. Nella classe di base, il membro della **proporzione** del messaggio di qualità è limitato a un intervallo di 500 (50%) a 2000 (200%). I valori non compresi in questo intervallo possono comportare modifiche di qualità improvvise.
3.  Per impostazione predefinita, il renderer video invia il messaggio di qualità al pin di output upstream (il pin connesso al pin di input). Le applicazioni possono eseguire l'override di questo comportamento **chiamando il metodo** SetValue.

Ciò che accade dopo dipende dal filtro upstream. Si tratta in genere di un filtro di trasformazione. La classe base per i filtri di trasformazione è [**CTransformFilter**](ctransformfilter.md), che usa le classi [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) per implementare i pin di input e di output. Insieme, queste classi hanno il seguente comportamento:

1.  Il metodo [**CTransformOutputPin:: Notify**](ctransformoutputpin-notify.md) chiama [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md), un metodo privato nella classe di base Filter.
2.  I filtri derivati possono eseguire l'override di **AlterQuality** per gestire il messaggio di qualità. Per impostazione predefinita, **AlterQuality** ignora il messaggio di qualità.
3.  Se **AlterQuality** non gestisce il messaggio di qualità, il pin di output chiama [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md), un metodo privato sul pin di input del filtro.
4.  **PassNotify** passa il messaggio di qualità al posto appropriato, ovvero il successivo pin di output upstream o un gestore qualità personalizzato.

Supponendo che nessun filtro di trasformazione gestisca il messaggio di qualità, il messaggio raggiunge infine il pin di output nel filtro di origine. Nelle classi base, [**CBasePin:: Notify**](cbasepin-notify.md) restituisce E \_ NOTIMPL. Il modo in cui un particolare filtro di origine gestisce i messaggi di qualità dipende dalla natura dell'origine. Alcune origini, ad esempio l'acquisizione video in tempo reale, non possono eseguire un controllo qualitativo significativo. Altre origini possono regolare la velocità con cui vengono recapitati i campioni.

Il diagramma seguente illustra il comportamento predefinito.

![controllo di qualità nelle classi di base](images/quality-control.png)

Il renderer video di base implementa **IQualityControl:: Notify**, il che significa che è possibile passare messaggi di qualità al renderer stesso. Se si imposta il membro della **proporzione** su un valore minore di 1000, il renderer video inserisce un periodo di attesa tra i frame che esegue il rendering, rallentando in effetti il renderer. Questa operazione può essere eseguita per ridurre l'utilizzo del sistema, ad esempio. Per ulteriori informazioni, vedere [**CBaseVideoRenderer:: ThrottleWait**](cbasevideorenderer-throttlewait.md). L'impostazione del membro della **proporzione** su un valore maggiore di 1000 non ha alcun effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione controllo qualità](quality-control-management.md)
</dt> </dl>

 

 



