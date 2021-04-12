---
description: Esempio di filtro di ambito
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Esempio di filtro di ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481517"
---
# <a name="scope-filter-sample"></a>Esempio di filtro di ambito

## <a name="description"></a>Descrizione

Il filtro ambito è un filtro renderer che Visualizza i dati audio come moduli Wave.

## <a name="usage"></a>Utilizzo

Per usare questo filtro, aprire GraphEdit ed eseguire il rendering di un file audio o di un file video con un flusso audio. Disconnettere temporaneamente il renderer audio e inserire il filtro di esempio Infinite-Pin Tee ([esempio di filtro InfTee](inftee-filter-sample.md)). Riconnettere il renderer audio. Connettere quindi il secondo pin di output del filtro Infinite-Pin tee al filtro ambito. A questo punto, eseguire il grafo.

La finestra ambito viene implementata come finestra di dialogo, non come finestra effettiva. Gli sviluppatori che creano pannelli di controllo per modificare i parametri di filtro in tempo reale potrebbero voler usare una tecnica come questa piuttosto che le pagine delle proprietà.

Il filtro di ambito illustra la configurazione di un thread separato per elaborare i dati. In questo caso, i dati vengono semplicemente copiati in un buffer separato nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) e vengono quindi disegnati sulla finestra ambito nel thread separato.

Il filtro ambito consente inoltre di monitorare l'output audio per determinare se si sta ritagliando, in modo da poter modificare il guadagno.

Questo filtro viene visualizzato in GraphEdit come "oscilloscopio".

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ directory radice \] SDK* \\ esempi di \\ \\ filtri DirectShow multimediali \\ \\ ambito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



