---
description: Specifica i dispositivi audio che il DSP di acquisizione vocale usa per l'acquisizione e il rendering dell'audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e9fd9eae8d53f1fa19bd8b55d94d292b9cd6cbf214b7a71a6473f1af647f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872994"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES

Specifica i dispositivi audio che il DSP di acquisizione vocale usa per l'acquisizione e il rendering dell'audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

(-1, -1).

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se si usa il provider di servizi di configurazione in modalità di origine. Il provider di servizi di dominio ignora questa proprietà in modalità filtro.

Il valore della proprietà è due WORD a 16 **bit,** suddivisi in un **valore DWORD.** I 16 bit superiori specificano il dispositivo di rendering audio (in genere un altoparlante) e i 16 bit inferiori specificano il dispositivo di acquisizione (in genere un microfono). Ogni dispositivo viene specificato come indice nella raccolta di dispositivi audio. Se l'indice è -1, viene usato il dispositivo predefinito.

L'indice del dispositivo corrisponde all'indice della raccolta usato [**nell'interfaccia IMMDeviceCollection.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) L'applicazione deve riprodurre la voce all'estremità attraverso il dispositivo di rendering selezionato. La voce all'estrema estremità è la voce della persona all'altra estremità della linea telefonica, che viene riprodotta tramite l'altoparlante sul computer dell'utente. Se il dispositivo di rendering selezionato non ha un flusso attivo, il DSP non può elaborare alcun output.

Il valore predefinito di questa proprietà è (-1, -1).

Nell'esempio seguente viene illustrato come inizializzare **l'oggetto PROPVARIANT** per questa proprietà.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Voice Capture DSP](voicecapturedmo.md)
</dt> </dl>

 

 
