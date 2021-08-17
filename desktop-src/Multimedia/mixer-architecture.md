---
title: Mixer Architettura
description: Mixer Architettura
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimediale, architettura mixer
- audio, architettura mixer
- mixer audio, architettura
- mixer audio, linee audio
- linee audio
- mixer audio, controlli
- audio multimediale, controlli mixer
- audio, controlli mixer
- mixer, linee audio
- mixer, architettura
- mixer, controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f435396dd2a8d5983f596628711dfd01afe7111e75af1dc2060f5c6c4ef0a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065611"
---
# <a name="mixer-architecture"></a>Mixer Architettura

L'elemento di base dell'architettura del mixer è una *linea audio*. Una linea audio è costituita da uno o più canali di dati provenienti da una singola origine o da una risorsa di sistema. Ad esempio, una linea audio stereo ha due canali di dati, ma è considerata una singola linea audio perché ha origine da una singola origine.

L'architettura del mixer fornisce servizi di routing per gestire le linee audio in un computer. È possibile usare i servizi di routing se sono installati dispositivi hardware e driver software adeguati. L'architettura del mixer consente a diverse linee di origine audio di eseguire il mapping a una singola linea audio di destinazione.

A ogni linea audio possono essere associati controlli mixer. Un controllo mixer può eseguire qualsiasi numero di funzioni (ad esempio il volume di controllo), a seconda delle caratteristiche della linea audio associata.

 

 




