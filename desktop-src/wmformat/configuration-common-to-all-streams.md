---
title: Configurazione comune a tutti Flussi
description: Configurazione comune a tutti Flussi
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profili,configurazioni comuni a tutti i flussi
- flussi, configurazioni comuni
- streams,names
- flussi, nomi di connessione
- flussi, numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e8b58e97ce2add4b6ff139aebacbc6d510af4424b2d3ae2bff3ea4577c429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964180"
---
# <a name="configuration-common-to-all-streams"></a>Configurazione comune a tutti Flussi

A tutti i flussi, indipendentemente dal tipo, devono essere assegnati un nome di flusso, un nome di connessione e un numero di flusso.

Il nome del flusso è semplicemente un nome descrittivo assegnato al flusso. Non è necessario che un flusso abbia un nome di flusso, ma consente di identificare il flusso durante la modifica del profilo in un secondo momento. È possibile impostare un nome per il flusso chiamando [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Ogni flusso deve avere un nome di connessione, denominato anche nome di input. Quando si imposta il profilo nell'oggetto writer per scrivere un file, il writer associa ogni nome di connessione a un input. Per identificare gli input, è necessario chiamare [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) per recuperare il nome della connessione. I nomi di connessione tipici sono semplici descrizioni del contenuto, ad esempio "audio". Se il profilo contiene flussi che si escludono a vicenda in base alla velocità in bit, ognuno dei flussi che si escludono a vicenda deve avere lo stesso nome di connessione. In caso contrario, il profilo non è valido e verrà rifiutato dal writer. È possibile impostare un nome di connessione chiamando [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

Il numero di flusso identifica il flusso all'interno del file. A differenza dei numeri di input e dei numeri di output, i numeri di flusso iniziano da 1, non da 0. Un numero di flusso è diverso da un indice di flusso, che viene utilizzato quando si ottengono flussi in un profilo usando [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). L'indice del flusso è un numero assegnato al flusso dall'oggetto profilo. Gli indici di flusso sono compresi tra 0 e uno minore del numero di flussi recuperati da [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). I numeri di flusso non devono essere sequenziali, anche se in genere lo sono e possono variare da 1 a 63. È possibile impostare un numero di flusso chiamando [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




