---
title: Configurazione comune a tutti i flussi
description: Configurazione comune a tutti i flussi
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profili, configurazioni comuni a tutti i flussi
- flussi, configurazioni comuni
- flussi, nomi
- flussi, nomi di connessione
- flussi, numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398786"
---
# <a name="configuration-common-to-all-streams"></a>Configurazione comune a tutti i flussi

A tutti i flussi, indipendentemente dal tipo, è necessario assegnare un nome di flusso, un nome di connessione e un numero di flusso.

Il nome del flusso è semplicemente un nome descrittivo assegnato al flusso. Un flusso non deve avere un nome di flusso, ma consente di identificare il flusso quando si modifica il profilo in un secondo momento. È possibile impostare un nome per il flusso chiamando [**IWMStreamConfig:: Sestreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Ogni flusso deve avere un nome di connessione, detto anche nome di input. Quando si imposta il profilo nell'oggetto writer per scrivere un file, il writer associa ogni nome di connessione a un input. Per identificare gli input, è necessario chiamare [**IWMInputMediaProps:: Getconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) per recuperare il nome della connessione. I nomi di connessione tipici sono semplici descrizioni del contenuto, ad esempio "audio". Se il profilo contiene flussi che si escludono a vicenda in base alla velocità in bit, ognuno dei flussi che si escludono a vicenda deve avere lo stesso nome di connessione. In caso contrario, il profilo non è valido e verrà rifiutato dal writer. È possibile impostare un nome di connessione chiamando [**IWMStreamConfig:: Seconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

Il numero di flusso identifica il flusso all'interno del file. A differenza dei numeri di input e dei numeri di output, i numeri di flusso iniziano da 1, non da 0. Un numero di flusso è diverso da un indice del flusso, che è possibile usare quando si recuperano i flussi in un profilo usando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). L'indice del flusso è un numero assegnato al flusso dall'oggetto profilo. Gli indici di flusso sono compresi tra 0 e uno inferiore al numero di flussi recuperato da [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). I numeri di flusso non devono essere sequenziali, anche se in genere sono e possono variare da 1 a 63. È possibile impostare un numero di flusso chiamando [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




