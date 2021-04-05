---
title: Uso degli output
description: Uso degli output
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, uso degli output
- Formato di sistemi avanzati (ASF), utilizzo degli output
- ASF (Advanced Systems Format), utilizzo di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri di output e formati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723455"
---
# <a name="working-with-outputs"></a>Uso degli output

Per impostazione predefinita, ogni esempio ricevuto da uno dei due oggetti Reader è associato a un numero di output. Ogni numero di output corrisponde a un flusso nel file ASF. Il lettore assegna i numeri di output ai flussi nel file quando il file viene aperto. In genere è presente un output per ogni flusso in un file. Se il file usa l'esclusione reciproca, tuttavia, a ogni gruppo di flussi che si escludono a vicenda viene assegnato un singolo numero di output. Il flusso che corrisponde al numero di output dei flussi che si escludono a vicenda è determinato dal lettore, nel caso di file con velocità in bit multipla (MBR) o dall'applicazione, se si utilizza la selezione del flusso manuale.

Poiché il nome della connessione impostato nel profilo non è salvato in modo permanente nel file, il Reader crea un nome di connessione predefinito per ogni output che è semplicemente una rappresentazione di stringa del numero di output, ad esempio "1", "2", "3" e così via. I nomi di connessione consentono alle applicazioni e al lettore stesso di correlare gli output ai flussi. In un file a più velocità in bit, diversi flussi condividono un nome di connessione. Questa operazione non è rilevante per il lettore, perché le proprietà di output per ogni flusso MBR sono identiche.

Ogni output ha uno o più formati di output supportati. Un formato di output è il formato utilizzato dai campioni non compressi forniti dal reader. Quando il lettore apre un file, imposta il formato di ogni output sul valore predefinito per il sottotipo di supporto. Il numero e il tipo di formati di output supportati sono determinati dal codec che decomprime i dati multimediali.

Negli argomenti seguenti viene illustrato come utilizzare gli output:

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

 

 




