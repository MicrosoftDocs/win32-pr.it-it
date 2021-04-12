---
description: Vantaggi di DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vantaggi di DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225458"
---
# <a name="benefits-of-dmos"></a>Vantaggi di DMOs

DMOs offre i vantaggi seguenti:

-   Sono in genere più piccoli e più semplici dei filtri DirectShow, perché supportano meno funzionalità.
-   Sono più flessibili dei filtri DirectShow perché non richiedono un grafico di filtro. È possibile usarli con DirectShow quando sono necessari i servizi forniti da DirectShow, ad esempio sincronizzazione, connessione intelligente, gestione automatica del flusso di dati e gestione dei thread. I client che non necessitano di questi servizi possono accedere direttamente a DMOs.
-   DMOs eseguono sempre l'elaborazione sincrona dei dati, che elimina molti dei problemi di threading che è necessario prendere in considerazione se si scrive un filtro.
-   A differenza dei codec ACM e VCM tradizionali, DMOs sono basati sulla Component Object Model (COM), quindi possono essere estesi tramite **QueryInterface**.
-   DMOs supporta un modello di streaming più generalizzato rispetto ai codec ACM o VCM. Analogamente ai filtri DirectShow, DMOs può supportare più input e più output.

Per questi motivi, è ora consigliabile usare DMOs come soluzione per la scrittura di codificatori, decodificatori e effetti audio. Sono possibili anche molti altri scenari, a seconda delle esigenze dell'applicazione.

Differenze tra DMOs e filtri DirectShow

I filtri DirectShow non possono funzionare al di fuori di un grafico filtro DirectShow. In DirectShow, il gestore del grafico del filtro intermedia tra l'applicazione e i filtri. I filtri DirectShow eseguono la maggior parte delle operazioni necessarie per lo streaming dei dati, tra cui:

-   Allocazione dei buffer.
-   Negoziazione di tipi di supporto e connessioni ad altri filtri.
-   Push dei dati tramite il grafico dei filtri.
-   Invio di eventi a Filter Graph Manager.
-   Sincronizzazione di più thread.

Al contrario, un DMO non esegue nessuna di queste operazioni. Questi tipi di attività sono invece responsabilità del client che utilizza DMO. Il client alloca i buffer, li compila con i dati e li recapita a DMO. Il DMO elabora i dati e il client recupera i buffer di output risultanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su DMOs](about-dmos.md)
</dt> </dl>

 

 



