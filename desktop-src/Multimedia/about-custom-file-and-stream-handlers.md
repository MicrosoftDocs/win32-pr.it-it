---
title: Informazioni sui gestori di file e flussi personalizzati
description: Informazioni sui gestori di file e flussi personalizzati
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video per Windows (VFW), gestori di file personalizzati
- Video per Windows (VFW), gestori di flussi personalizzati
- Video per Windows (VFW), gestori di file
- Video per Windows (VFW), gestori di flusso
- VFW (video per Windows), gestori di file personalizzati
- VFW (video per Windows), gestori di flussi personalizzati
- VFW (video per Windows), gestori di file
- VFW (video per Windows), gestori di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856917"
---
# <a name="about-custom-file-and-stream-handlers"></a>Informazioni sui gestori di file e flussi personalizzati

L'applicazione può usare un gestore di file personalizzato per leggere da un file o scrivere in un file in un formato non standard. A tale scopo, l'applicazione usa semplicemente il nome del gestore di file quando si apre il file o si alloca l'interfaccia del file. La libreria AVIFile usa quindi le funzioni del gestore di file anziché quelle di un altro gestore di file. Il formato non standard viene visualizzato come dati AVI standard nell'applicazione o in qualsiasi altra applicazione che usa il gestore di file personalizzato.

Analogamente, l'applicazione può usare un gestore di flusso personalizzato per leggere un flusso in un formato non standard. Un flusso, indipendentemente dal fatto che sia costituito da dati audio, video, MIDI, testo o personalizzati, è un componente di un file AVI. Ad esempio, un file AVI che contiene una sequenza video, una colonna inglese e una colonna musicale francese è costituito da tre flussi. L'applicazione può specificare i flussi in un file AVI per elaborare e indirizzare ognuno di questi flussi a un gestore che può elaborare in modo ottimale il tipo di dati multimediali appropriato.

> [!Note]  
> È necessario inserire gestori di file e di flusso personalizzati in una o più dll, separate dai file dell'applicazione principale.

 

 

 




