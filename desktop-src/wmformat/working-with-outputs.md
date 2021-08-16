---
title: Uso degli output
description: Uso degli output
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, uso degli output
- Advanced Systems Format (ASF), uso degli output
- ASF (Advanced Systems Format), uso degli output
- Advanced Systems Format (ASF), numeri di output e formati
- ASF (Advanced Systems Format), numeri di output e formati
- formati e numeri di output, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e5b4980ef14126006d3f19fe0717aa9eb6fd5c1a8f7baaf91e35084faeacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697725"
---
# <a name="working-with-outputs"></a>Uso degli output

Come impostazione predefinita, ogni campione ricevuto da uno degli oggetti reader è associato a un numero di output. Ogni numero di output corrisponde a un flusso nel file ASF. Il lettore assegna i numeri di output ai flussi nel file quando il file viene aperto. In genere è presente un output per ogni flusso in un file. Se il file usa l'esclusione reciproca, a ogni gruppo di flussi che si escludono a vicenda viene assegnato un singolo numero di output. Il flusso che corrisponde al numero di output dei flussi che si escludono a vicenda è determinato dal lettore, nel caso di più file MBR (Bit Rate) o dall'applicazione, se si usa la selezione manuale del flusso.

Poiché il nome di connessione impostato nel profilo non è persistente nel file, il lettore crea un nome di connessione predefinito per ogni output che è semplicemente una rappresentazione di stringa del numero di output, ad esempio "1", "2", "3" e così via. I nomi di connessione consentono alle applicazioni e al lettore stesso di correlare gli output ai flussi. In un file a velocità in bit multipla, diversi flussi condividono un nome di connessione. Questo non è importante per il lettore, perché le proprietà di output per ogni flusso MBR sono identiche.

Ogni output ha uno o più formati di output supportati. Un formato di output è il formato utilizzato dagli esempi non compressi forniti dal lettore. Quando il lettore apre un file, imposta il formato di ogni output sul valore predefinito per il sottotipo multimediale. Il numero e il tipo di formati di output supportati sono determinati dal codec che decomprime i dati multimediali.

Negli argomenti seguenti viene illustrato come usare gli output:

-   [Per identificare i numeri di output](to-identify-output-numbers.md)
-   [Assegnazione di formati di output](assigning-output-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




