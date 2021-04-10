---
description: Ripristino da un errore di Invalid-Device (audio spaziale)
title: Ripristino da un errore di Invalid-Device (audio spaziale)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127423"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Ripristino da un errore di Invalid-Device (audio spaziale)

Molti dei metodi dell'API Microsoft spatial audio, ad esempio [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), restituiscono i codici di errore se il dispositivo dell'endpoint audio utilizzato dall'applicazione client diventa non valido o il formato di rendering dell'audio spaziale viene modificato nell'endpoint. Questi codici di errore indicano che il dispositivo endpoint è stato scollegato o che l'hardware audio o le risorse hardware associate sono state riconfigurate, disabilitate, rimosse, la modalità audio spaziale viene modificata o non è disponibile per l'utilizzo. Spesso l'applicazione può risolvere questo errore.

I codici di errore che indicano un errore di dispositivo non valido includono i seguenti:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Strategie per la gestione di errori di dispositivo non valido

La strategia consigliata per il ripristino da un errore di dispositivo non valido dipende dal fatto che l'applicazione selezioni automaticamente un dispositivo specifico in base ai requisiti interni o che consenta all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili. 

### <a name="default-audio-device"></a>Dispositivo audio predefinito

Se l'applicazione seleziona automaticamente il dispositivo predefinito, attenersi alla procedura seguente per eseguire il ripristino.

1. Rilasciare l'interfaccia [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) e tutte le altre interfacce audio spaziali utilizzate per il rendering. 
1. Chiamare [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo audio predefinito corrente.
1. Tentativo di attivare **ISpatialAudioClient** sul dispositivo audio.
1. Attivare **ISpatialAudioObjectRenderStream**. 

### <a name="specifically-selected-audio-device"></a>Dispositivo audio selezionato in modo specifico

Se l'applicazione seleziona un dispositivo audio specifico, attenersi alla procedura seguente per eseguire il ripristino.

1. Rilasciare l'interfaccia ISpatialAudioObjectRenderStream e tutte le altre interfacce audio spaziali usate per il rendering, ma non rilasciare **ISpatialAudioClient**.
1. Usare l'istanza corrente di **ISpatialAudioClient** per attivare **ISpatialAudioObjectRenderStream**.

Si noti che per entrambe le strategie elencate in precedenza, è possibile applicare gli stessi passaggi alle applicazioni che usano le interfacce [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) . È sufficiente sostituire **ISpatialAudioObjectRenderStream** nei passaggi precedenti con le interfacce Metadata o HRTF.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>
[Ripristino da un errore](recovering-from-an-invalid-device-error.md) 
 di Invalid-Device [Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



