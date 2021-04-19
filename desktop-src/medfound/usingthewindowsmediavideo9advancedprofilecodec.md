---
description: Uso del profilo avanzato Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del profilo avanzato Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320518"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Uso del profilo avanzato Windows Media Video 9

Le procedure video di base descritte nella sezione [utilizzo del video](workingwithvideo.md) si applicano anche direttamente al profilo avanzato Windows Media video 9. Non sono necessarie procedure particolari.

Il profilo avanzato Windows Media Video 9 è associato agli identificatori di classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject. Il valore di FOURCC per i tipi di supporto che usano questo codec è "WVC1".

Il profilo avanzato Windows Media Video 9 supporta tutte le modalità di codifica comuni, nonché la codifica interlacciata, la codifica mista interlacciata e progressiva, le risoluzioni diverse dalle funzionalità di visualizzazione e riduzione degli intervalli. Un'altra funzionalità è la possibilità di archiviare i metadati di sequenza e frame nel flusso di bit stesso; in precedenza era necessario usare l'API ASF e le estensioni di unità dati.

Le seguenti proprietà del profilo avanzato Windows Media Video 9, che può essere controllato usando le impostazioni del registro di sistema, non hanno stringhe **IPropertyBag** o **IPropertyStore** corrispondenti:

-   Opzione DQuant.
-   DQuant livello di attendibilità.
-   Forza sovrapposizione.
-   Metodo di costo del vettore di movimento.

## <a name="achieving-optimal-visual-quality"></a>Ottenere qualità visiva ottimale

Per la maggior parte dei dati video, per ottenere una qualità visiva ottimale usando il profilo avanzato Windows Media Video 9, è possibile impostare la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) su 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Informazioni sui codec precedenti del profilo avanzato Windows Media Video 9

La versione corrente del codec del profilo avanzato Windows Media Video 9 è basata sulla società di Motion Picture and Television Engineers (SMPTE) standard per il profilo avanzato VC-1 (SMPTE 421M). Questo codec sostituisce il codec precedente di Windows, detto anche Windows Media Video 9 Advanced Profile codec, identificato dal codice FOURCC "WMVA". La versione precedente del codec VC-1 è stata implementata prima che lo standard del profilo avanzato VC-1 venisse finalizzato e non è più supportato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> 
<dt>

[Uso delle impostazioni avanzate del codec del profilo avanzato Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



