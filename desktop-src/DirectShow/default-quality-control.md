---
description: Controllo qualità predefinito
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Controllo qualità predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df737855376db52a35476c0f01da4b850e3678ec20595ee82720b7b928237ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953135"
---
# <a name="default-quality-control"></a>Controllo qualità predefinito

Le [DirectShow base implementano](directshow-base-classes.md) alcuni comportamenti predefiniti per il controllo della qualità video.

I messaggi di qualità iniziano dal renderer. La classe di base per i renderer video [**è CBaseVideoRenderer**](cbasevideorenderer.md), che presenta il comportamento seguente:

1.  Quando il renderer video riceve un esempio, confronta il timestamp dell'esempio con l'ora di riferimento corrente.
2.  Il renderer video genera un messaggio di qualità. Nella classe di base il membro **Proportion** del messaggio di qualità è limitato a un intervallo compreso tra 500 (50%) e 2000 (200%). I valori al di fuori di questo intervallo possono comportare modifiche di qualità improvva.
3.  Per impostazione predefinita, il renderer video invia il messaggio di qualità al pin di output upstream (il pin connesso al pin di input). Le applicazioni possono eseguire l'override di questo comportamento chiamando **il metodo SetSink.**

L'operazione successiva dipende dal filtro upstream. In genere, si tratta di un filtro di trasformazione. La classe di base per i filtri di trasformazione è [**CTransformFilter,**](ctransformfilter.md)che usa le classi [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) per implementare i pin di input e output. Insieme, queste classi hanno il comportamento seguente:

1.  Il [**metodo CTransformOutputPin::Notify**](ctransformoutputpin-notify.md) chiama [**CTransformFilter::AlterQuality,**](ctransformfilter-alterquality.md)un metodo privato nella classe di base del filtro.
2.  I filtri derivati possono eseguire **l'override di AlterQuality** per gestire il messaggio di qualità. Per impostazione predefinita, **AlterQuality** ignora il messaggio di qualità.
3.  Se **AlterQuality** non gestisce il messaggio di qualità, il pin di output chiama [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md), un metodo privato sul pin di input del filtro.
4.  **PassNotify** passa il messaggio di qualità alla posizione appropriata, ovvero il pin di output upstream successivo o un gestore qualità personalizzato.

Supponendo che nessun filtro di trasformazione gestisca il messaggio di qualità, il messaggio raggiungerà infine il pin di output nel filtro di origine. Nelle classi di base [**CBasePin::Notify**](cbasepin-notify.md) restituisce E \_ NOTIMPL. Il modo in cui un determinato filtro di origine gestisce i messaggi di qualità dipende dalla natura dell'origine. Alcune origini, ad esempio l'acquisizione di video live, non possono eseguire un controllo di qualità significativo. Altre origini possono regolare la frequenza con cui recapitare i campioni.

Il diagramma seguente illustra il comportamento predefinito.

![controllo di qualità nelle classi di base](images/quality-control.png)

Il renderer video di base implementa **IQualityControl::Notify,** il che significa che è possibile passare messaggi di qualità al renderer stesso. Se si imposta il membro **Proportion** su un valore minore di 1000, il renderer video inserisce un periodo di attesa tra ogni fotogramma di cui viene eseguito il rendering, rallentando di fatto il renderer. Ad esempio, è possibile eseguire questa operazione per ridurre l'utilizzo del sistema. Per altre informazioni, vedere [**CBaseVideoRenderer::ThrottleWait.**](cbasevideorenderer-throttlewait.md) **L'impostazione del** membro Proportion su un valore maggiore di 1000 non ha alcun effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione del controllo di qualità](quality-control-management.md)
</dt> </dl>

 

 



