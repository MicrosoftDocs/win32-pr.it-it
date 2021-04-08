---
description: Specifica i dispositivi audio usati dal DSP di acquisizione vocale per l'acquisizione e il rendering dell'audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Proprietà MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880082"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>\_Proprietà degli \_ indici del dispositivo WMAAECMA di MFPKEY \_

Specifica i dispositivi audio usati dal DSP di acquisizione vocale per l'acquisizione e il rendering dell'audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

(-1,-1).

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se si utilizza il DSP in modalità origine. Il DSP ignora questa proprietà in modalità filtro.

Il valore della proprietà è costituito da **parole** a 2 16 bit compresse in un valore **DWORD**. I 16 bit superiori specificano il dispositivo di rendering audio (in genere un altoparlante) e i 16 bit inferiori specificano il dispositivo di acquisizione (in genere un microfono). Ogni dispositivo viene specificato come indice nella raccolta di dispositivi audio. Se l'indice è-1, viene usato il dispositivo predefinito.

L'indice del dispositivo corrisponde all'indice della raccolta usato nell'interfaccia [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . L'applicazione deve riprodurre la voce finale tramite il dispositivo di rendering selezionato. (La voce finale è la voce della persona sull'altra estremità della linea telefonica, che viene riprodotta attraverso l'altoparlante sul computer dell'utente). Se il dispositivo di rendering selezionato non dispone di un flusso attivo, il DSP non può elaborare alcun output.

Il valore predefinito di questa proprietà è (-1,-1).

Nell'esempio seguente viene illustrato come inizializzare **PROPVARIANT** per questa proprietà.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
