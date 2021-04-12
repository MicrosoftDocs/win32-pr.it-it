---
title: Modelli di conformità del dispositivo
description: Modelli di conformità del dispositivo
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK, modelli di conformità del dispositivo
- codec, modelli di conformità del dispositivo
- modelli di conformità del dispositivo, informazioni
- modelli, modelli di conformità dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332327"
---
# <a name="device-conformance-templates"></a>Modelli di conformità del dispositivo

I codec della serie Windows Media 9 supportano i modelli di conformità dei dispositivi, che sono intervalli definiti di impostazioni di configurazione del flusso e algoritmi di codec. Ogni modello definisce gli intervalli di valori appropriati per determinati dispositivi.

In passato, i produttori di hardware che rendevano i dispositivi in grado di riprodurre file ASF venivano tutti applicati ai propri standard. Ciò ha comportato una gamma molto diversificata di funzionalità su dispositivi simili che continuano a essere attuali.

Con i modelli di conformità dei dispositivi, i codec Windows Media stabiliscono un terreno comune per dispositivi simili. I produttori di hardware possono indicare a quali modelli sono conformi i loro dispositivi, consentendo agli autori di contenuti di indirizzare i file in modo più sicuro alla lettura dei dispositivi. È inoltre più facile per le applicazioni del lettore determinare se un file non è appropriato per il dispositivo prima di provare a riprodurlo.

Un modello di conformità del dispositivo è identificato da una stringa, archiviata come un attributo di metadati associato al flusso a cui si applica il modello. Per un elenco dei modelli e delle relative stringhe e parametri, vedere [parametri del modello di conformità del dispositivo](device-conformance-template-parameters.md).

I modelli di conformità dei dispositivi sono supportati per tutti i codec Windows Media 9 e versioni successive, ad eccezione del codec Windows Media Video 9 screen e del codec Windows Media Audio 9 Lossless.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> <dt>

[**Uso dei modelli di conformità dei dispositivi**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




