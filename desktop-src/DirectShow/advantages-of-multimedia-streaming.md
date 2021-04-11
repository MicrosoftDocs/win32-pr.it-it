---
description: Vantaggi dello streaming multimediale
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantaggi dello streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132158"
---
# <a name="advantages-of-multimedia-streaming"></a>Vantaggi dello streaming multimediale

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Quando gli sviluppatori usano lo streaming multimediale nelle proprie applicazioni, riduce notevolmente la quantità di programmazione specifica del formato necessario. In genere, un'applicazione che deve ottenere i dati multimediali da un file o da un'origine hardware deve conoscere tutte le informazioni sul formato dei dati e sul dispositivo hardware. L'applicazione deve gestire la connessione, il trasferimento dei dati, qualsiasi conversione di dati necessaria e l'archiviazione di file o il rendering dei dati effettivi. Poiché ogni formato e dispositivo è leggermente diverso, questo processo è spesso complesso e ingombrante. Il flusso multimediale, d'altra parte, negozia automaticamente il trasferimento e la conversione dei dati dall'origine all'applicazione. Le interfacce di flusso offrono un metodo uniforme e prevedibile di accesso ai dati e controllo, che consente a un'applicazione di riprodurre i dati, indipendentemente dall'origine o dal formato originale.

I passaggi seguenti illustrano come implementare lo streaming, dal dispositivo hardware alla riproduzione di cui è stato eseguito il rendering.

1.  Un'origine di dati video, ad esempio DirectShow, espone le interfacce di streaming.
2.  Lo sviluppatore di applicazioni usa le interfacce di streaming multimediali per gestire la conversione del formato dati.
3.  Lo sviluppatore di applicazioni utilizza le interfacce DirectDraw per eseguire il rendering dei dati risultanti.

La specifica per i flussi multimediali comprende diverse interfacce. ogni interfaccia include metodi che controllano un determinato aspetto del processo di streaming o gestiscono un determinato tipo di dati. Per ulteriori informazioni, vedere l' [elenco delle interfacce di streaming multimediali](list-of-multimedia-streaming-interfaces.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'architettura di streaming multimediale](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



