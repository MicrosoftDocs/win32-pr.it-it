---
description: In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227067"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?

Il numero di frame di un flusso codificato può essere inferiore al numero di frame dell'originale per uno dei due motivi seguenti: frame duplicati e frame eliminati.

Il codificatore non produce in genere frame che sono duplicati esatti del frame precedente. Se è necessario disporre di un campione per ogni frame (ad esempio, è necessario per alcuni contenitori), è possibile configurare il codificatore per produrre frame "fittizi" impostando la proprietà [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su Variant \_ true.

Il codificatore rilascia frame quando non è in grado di codificare tutti i frame senza overflow del buffer. I frame eliminati influiscono sulla qualità del flusso. i frame duplicati non lo fanno.

È possibile ottenere le statistiche del frame dal codificatore per determinare se i frame sono stati eliminati. Per ulteriori informazioni, vedere [recupero delle statistiche di codifica](gettingencodingstatistics.md).

In genere, i flussi VBR basati sulla qualità avranno un numero di frame inferiore rispetto a quello originale se sono presenti frame duplicati (poiché la velocità in bit non è vincolata).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 



