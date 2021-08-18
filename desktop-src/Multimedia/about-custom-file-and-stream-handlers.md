---
title: Informazioni sui gestori di file e flussi personalizzati
description: Informazioni sui gestori di file e flussi personalizzati
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video per Windows (VFW), gestori di file personalizzati
- Video per Windows (VFW), gestori di flussi personalizzati
- Video per Windows (VFW), gestori di file
- Video per Windows (VFW), gestori di flussi
- VFW (Video per Windows),gestori di file personalizzati
- VFW (Video per Windows),gestori di flussi personalizzati
- VFW (Video per Windows),gestori di file
- VFW (Video per Windows),gestori di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719c5312c5ba1e783e0cd4cdb81565f66241e4662772ca441283571f0335fb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145159"
---
# <a name="about-custom-file-and-stream-handlers"></a>Informazioni sui gestori di file e flussi personalizzati

L'applicazione può usare un gestore di file personalizzato per leggere da un file o scrivere in un file in un formato non standard. A tale scopo, l'applicazione usa semplicemente il nome del gestore di file quando si apre il file o si alloca l'interfaccia del file. La libreria AVIFile usa quindi le funzioni del gestore di file anziché quelle di un altro gestore di file. Il formato non standard viene visualizzato come dati AVI standard per l'applicazione o per qualsiasi altra applicazione che usa il gestore di file personalizzato.

Analogamente, l'applicazione può usare un gestore di flusso personalizzato per leggere un flusso in un formato non standard. Un flusso, che sia audio, video, MIDI, testo o dati personalizzati, è un componente di un file AVI. Ad esempio, un file AVI che contiene una sequenza video, un inglese e un francese sono costituiti da tre flussi. L'applicazione può specificare i flussi in un file AVI per elaborare e indirizzare ognuno di questi flussi a un gestore in grado di elaborare in modo ottimale il tipo appropriato di dati multimediali.

> [!Note]  
> È necessario inserire gestori di flussi e file personalizzati in una o più DLL, separate dai file principali dell'applicazione.

 

 

 




