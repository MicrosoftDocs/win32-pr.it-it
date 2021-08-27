---
description: Vantaggi delle dmo
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vantaggi delle dmo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b13a9ef7f91446d03732b935648b689ab65a33c9d10dcfca26051d9284404db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103371"
---
# <a name="benefits-of-dmos"></a>Vantaggi delle dmo

Le viste a gestione dinamica offrono i vantaggi seguenti:

-   Sono in genere più piccoli e più semplici rispetto DirectShow, perché supportano meno funzionalità.
-   Sono più flessibili rispetto ai DirectShow perché non richiedono un grafico dei filtri. È possibile usarli con DirectShow quando sono necessari i servizi forniti da DirectShow, ad esempio la sincronizzazione, la connessione intelligente, la gestione automatica del flusso di dati e la gestione dei thread. I client che non necessitano di questi servizi possono accedere direttamente agli oggetti DMO.
-   Gli oggetti DMO eseguono sempre l'elaborazione dei dati sincrona, eliminando così molti dei problemi di threading che è necessario considerare se si scrive un filtro.
-   A differenza dei codec ACM e VCM tradizionali, gli oggetti DMO sono basati sul Component Object Model (COM), quindi possono essere estesi tramite **QueryInterface.**
-   I DMO supportano un modello di streaming più generalizzato rispetto ai codec ACM o VCM. Analogamente DirectShow filtri, gli oggetti DMO possono supportare più input e più output.

Per questi motivi, gli oggetti DMO sono ora consigliati come soluzione per la scrittura di codificatori, decodificatori ed effetti audio. Sono possibili anche molti altri scenari, a seconda delle esigenze dell'applicazione.

Differenze tra dmo e filtri DirectShow dati

DirectShow filtri non possono funzionare all'esterno di un DirectShow di filtro. In DirectShow, Filter Graph Manager media tra l'applicazione e i filtri. DirectShow filtri eseranno la maggior parte delle operazioni necessarie per trasmettere i dati, tra cui:

-   Allocazione di buffer.
-   Negoziazione di tipi di supporti e connessioni ad altri filtri.
-   Push dei dati tramite il grafico del filtro.
-   Invio di eventi a Filter Graph Manager.
-   Sincronizzazione di più thread.

Al contrario, una DMO esegue nessuna di queste operazioni. Questi tipi di attività sono invece responsabilità del client che usa il DMO. Il client alloca i buffer, li riempie di dati e li recapita al DMO. Il DMO elabora i dati e il client recupera i buffer di output risultanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sugli oggetti DMO](about-dmos.md)
</dt> </dl>

 

 



