---
description: Uso del profilo Windows Media Video 9 Advanced
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del profilo Windows Media Video 9 Advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258c32f14d1a7a42e1450c8265e2a611bd17b3b92b98f5433c93b91251e299c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012171"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Uso del profilo Windows Media Video 9 Advanced

Le procedure video di base descritte nella sezione Uso dei [video](workingwithvideo.md) si applicano anche direttamente al profilo Windows Profilo avanzato di Media Video 9. Non sono necessarie procedure speciali.

Il Windows profilo avanzato di Media Video 9 è associato agli identificatori di classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject. Il valore FOURCC per i tipi di supporti che usano questo codec è "WVC1".

Il profilo avanzato di Windows Media Video 9 supporta tutte le modalità di codifica comuni, nonché la codifica interlacciata, la codifica mista interlacciata e progressiva, le risoluzioni diverse rispetto alla visualizzazione e le funzionalità di riduzione dell'intervallo. Un'altra funzionalità è la possibilità di archiviare metadati di sequenza e frame nel flusso di bit stesso; in precedenza era necessario usare l'API ASF e Data Unit Extensions.

Le proprietà seguenti del profilo Windows Media Video 9 Advanced, che possono essere controllate usando le impostazioni del Registro di sistema, non hanno stringhe **IPropertyBag** o **IPropertyStore** corrispondenti:

-   Opzione Dquant.
-   Intensità dquant.
-   Forza sovrapposizione.
-   Metodo di costo del vettore di movimento.

## <a name="achieving-optimal-visual-quality"></a>Ottenere una qualità visiva ottimale

Per la maggior parte dei dati video, per ottenere una qualità visiva ottimale usando il profilo avanzato di Windows Media Video 9, è possibile impostare la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) su 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Informazioni sui codec Windows Media Video 9 Advanced Profile

La versione corrente del codec Windows Media Video 9 Advanced Profile è basata sullo standard SMPTE (Society of Motion Picture and Television Engineers) per vc-1 (SMPTE 421M) Advanced Profile. Questo codec sostituisce il codec precedente Windows denominato anche codec profilo avanzato Windows Media Video 9, identificato dal codice FOURCC "WMVA". La versione precedente del codec VC-1 è stata implementata prima della finalizzazione dello standard del profilo avanzato VC-1 e non è più supportata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> 
<dt>

[Uso dell'Impostazioni del codec Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



