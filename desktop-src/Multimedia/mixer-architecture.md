---
title: Architettura mixer
description: Architettura mixer
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimediale, architettura mixer
- audio, architettura mixer
- mixer audio, architettura
- mixer audio, linee audio
- linee audio
- mixer audio, controlli
- audio multimediale, controlli Mixer
- audio, controlli Mixer
- mixer, linee audio
- mixer, architettura
- mixer, controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329783"
---
# <a name="mixer-architecture"></a>Architettura mixer

L'elemento di base dell'architettura del mixer è una *linea audio*. Una linea audio è costituita da uno o più canali di dati originati da una singola origine o da una risorsa di sistema. Una linea audio stereo, ad esempio, ha due canali di dati, ma viene considerata come una singola riga audio, perché ha origine da un'unica origine.

L'architettura del mixer fornisce servizi di routing per gestire le linee audio in un computer. È possibile utilizzare i servizi di routing se sono installati dispositivi hardware e driver software appropriati. L'architettura del mixer consente di eseguire il mapping di diverse righe di origine audio a una singola riga audio di destinazione.

A ogni linea audio possono essere associati controlli mixer. Un controllo mixer può eseguire un numero qualsiasi di funzioni, ad esempio il volume di controllo, a seconda delle caratteristiche della linea audio associata.

 

 




