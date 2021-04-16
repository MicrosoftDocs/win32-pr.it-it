---
description: Supporto MPEG-2 in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Supporto MPEG-2 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522194"
---
# <a name="mpeg-2-support-in-directshow"></a>Supporto MPEG-2 in DirectShow

Questa sezione descrive i componenti che è possibile usare per riprodurre contenuto MPEG-2 in DirectShow.

> [!Note]  
> Sebbene il video DVD si basi su MPEG-2, in questa sezione non viene descritta la riproduzione o la navigazione in DVD. Per informazioni sui DVD in DirectShow, vedere [applicazioni DVD](dvd-applications.md).

 

I dati MPEG-2 possono provenire da un file locale o da un'origine live, ad esempio una trasmissione di rete o un dispositivo D-VHS. La riproduzione dei file è detta *modalità pull* , perché il filtro del parser estrae i dati dal file nel grafico dei filtri. Le origini attive sono denominate *modalità push* perché il filtro di origine inserisce i dati nel grafico.

DirectShow fornisce due filtri che consentono di analizzare i flussi di sistema MPEG-2:

-   [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): questo filtro supporta la modalità push per flussi di programma e flussi di trasporto. In Windows XP e versioni successive, supporta anche la modalità pull per i flussi di programma.
-   [Splitter MPEG-2](mpeg-2-splitter.md): questo filtro supporta la modalità pull per i flussi di programma sulle piattaforme di livello inferiore. Questo filtro è deprecato in Windows XP e versioni successive.

Per usare il separatore MPEG-2 demux o MPEG-2, è necessario disporre di decodificatori audio e video MPEG-2 compatibili con DirectShow che accettano i flussi elementari (PES).

Questa sezione contiene i seguenti argomenti:

-   [Panoramica dei sistemi MPEG-2](overview-of-mpeg-2-systems.md)
-   [Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Uso della barra di divisione MPEG-2](using-the-mpeg-2-splitter.md)
-   [Proprietà di esempio MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



