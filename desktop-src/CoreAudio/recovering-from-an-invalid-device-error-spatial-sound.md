---
description: Ripristino da un errore Invalid-Device (suono spaziale)
title: Ripristino da un errore Invalid-Device (suono spaziale)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 124d4a804c2f99c051fee50d1c8d819d794b87a5943c216951e0c72870de8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406219"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Ripristino da un errore Invalid-Device (suono spaziale)

Molti dei metodi dell'API Audio spaziale Microsoft, ad esempio [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), restituiscono codici di errore se il dispositivo endpoint audio in uso dall'applicazione client diventa non valido o il formato di rendering audio spaziale viene modificato nell'endpoint. Questi codici di errore indicano che il dispositivo endpoint è stato scollegato o che l'hardware audio o le risorse hardware associate sono stati riconfigurati, disabilitati, rimossi, la modalità audio spaziale è stata modificata o altrimenti resa non disponibile per l'uso. Spesso l'applicazione può eseguire il ripristino da questo errore.

I codici di errore che indicano un errore di dispositivo non valido includono quanto segue:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Strategie per la gestione degli errori di dispositivo non valido

La strategia consigliata per il ripristino da un errore di dispositivo non valido dipende dal fatto che l'applicazione seleziona automaticamente un dispositivo specifico in base ai requisiti interni o consenta all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili. 

### <a name="default-audio-device"></a>Dispositivo audio predefinito

Se l'applicazione seleziona automaticamente il dispositivo predefinito, seguire questa procedura per eseguire il ripristino.

1. Rilasciare [l'interfaccia ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) e qualsiasi altra interfaccia audio spaziale usata per il rendering. 
1. Chiamare [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo audio predefinito corrente.
1. Provare ad attivare **ISpatialAudioClient** nel dispositivo audio.
1. Attivare **ISpatialAudioObjectRenderStream.** 

### <a name="specifically-selected-audio-device"></a>Dispositivo audio selezionato in modo specifico

Se l'applicazione seleziona un dispositivo audio specifico, seguire questa procedura per eseguire il ripristino.

1. Rilasciare l'interfaccia ISpatialAudioObjectRenderStream e qualsiasi altra interfaccia audio spaziale usata per il rendering, ma non **rilasciare ISpatialAudioClient.**
1. Usare **l'istanza corrente di ISpatialAudioClient** per attivare **ISpatialAudioObjectRenderStream.**

Si noti che per entrambe le strategie elencate in precedenza, gli stessi passaggi possono essere applicati alle applicazioni che usano le interfacce [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf.](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) È sufficiente **sostituire ISpatialAudioObjectRenderStream** nei passaggi precedenti con i metadati o le interfacce Hrtf.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>
[Ripristino da un errore Invalid-Device errore](recovering-from-an-invalid-device-error.md) 
 [Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



