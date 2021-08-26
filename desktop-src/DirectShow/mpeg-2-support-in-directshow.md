---
description: Supporto mpeg-2 in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Supporto mpeg-2 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9feaa24ea36b6f5e00e0f6ecd5db49ce37181f9d6d7348b3cfa27e64f7f2d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075801"
---
# <a name="mpeg-2-support-in-directshow"></a>Supporto mpeg-2 in DirectShow

Questa sezione descrive i componenti che è possibile usare per riprodurre contenuto MPEG-2 in DirectShow.

> [!Note]  
> Anche se il video DVD è basato su MPEG-2, questa sezione non descrive la riproduzione o la navigazione dei DVD. Per informazioni su DVD in DirectShow, vedere [Applicazioni DVD](dvd-applications.md).

 

I dati MPEG-2 possono provengono da un file locale o da un'origine live, ad esempio una trasmissione di rete o un dispositivo D-VHS. La riproduzione di file è *detta modalità pull* perché il filtro del parser estrae i dati dal file nel grafico dei filtri. Le origini in tempo reale sono *chiamate modalità push* perché il filtro di origine inserisce i dati nel grafico.

DirectShow fornisce due filtri in grado di analizzare i flussi di sistema MPEG-2:

-   [MpEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): questo filtro supporta la modalità push per i flussi di programma e i flussi di trasporto. In Windows XP e versioni successive supporta anche la modalità pull per i flussi di programma.
-   [Splitter MPEG-2:](mpeg-2-splitter.md)questo filtro supporta la modalità pull per i flussi di programma nelle piattaforme di livello inferiore. Questo filtro è deprecato in Windows XP e versioni successive.

Per usare il demux MPEG-2 o lo splitter MPEG-2, è necessario disporre di decodificatori audio e video MPEG-2 compatibili con DirectShow che accettano flussi elementari in pacchetto (PES).

Questa sezione contiene i seguenti argomenti:

-   [Panoramica dei sistemi MPEG-2](overview-of-mpeg-2-systems.md)
-   [Uso del demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Uso della barra di divisione MPEG-2](using-the-mpeg-2-splitter.md)
-   [Proprietà di esempio MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



