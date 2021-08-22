---
description: Vantaggi dello streaming multimediale
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantaggi dello streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537541"
---
# <a name="advantages-of-multimedia-streaming"></a>Vantaggi dello streaming multimediale

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Grabber**](sample-grabber-filter.md) di esempio o implementare un filtro personalizzato per ottenere dati da un DirectShow di filtro.

 

Quando gli sviluppatori usano lo streaming multimediale nelle applicazioni, riduce notevolmente la quantità di programmazione specifica del formato necessaria. In genere, un'applicazione che deve ottenere dati multimediali da un file o da un'origine hardware deve conoscere tutto il formato dei dati e il dispositivo hardware. L'applicazione deve gestire la connessione, il trasferimento dei dati, qualsiasi conversione di dati necessaria e il rendering effettivo dei dati o l'archiviazione di file. Poiché ogni formato e dispositivo è leggermente diverso, questo processo è spesso complesso e complesso. Lo streaming multimediale, d'altra parte, negozia automaticamente il trasferimento e la conversione dei dati dall'origine all'applicazione. Le interfacce di streaming forniscono un metodo uniforme e prevedibile di accesso e controllo dei dati, che semplifica la riproduzione dei dati da parte di un'applicazione, indipendentemente dall'origine o dal formato originale.

La procedura seguente illustra come implementare lo streaming, dal dispositivo hardware alla riproduzione sottoposta a rendering.

1.  Un'origine di dati video, ad esempio DirectShow, espone le interfacce di streaming.
2.  Lo sviluppatore dell'applicazione usa le interfacce di streaming multimediali per gestire la conversione del formato dei dati.
3.  Lo sviluppatore dell'applicazione usa le interfacce DirectDraw per eseguire il rendering dei dati risultanti.

La specifica per i flussi multimediali include diverse interfacce. ogni interfaccia include metodi che controllano un determinato aspetto del processo di streaming o gestiscono un determinato tipo di dati. Per [altre informazioni, vedere Elenco di](list-of-multimedia-streaming-interfaces.md) interfacce di streaming multimediali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'architettura di streaming multimediale](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



