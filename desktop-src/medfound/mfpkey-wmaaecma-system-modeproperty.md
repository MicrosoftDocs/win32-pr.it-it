---
description: Imposta la modalità di elaborazione per il DSP di acquisizione voce.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973270"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE

Imposta la modalità di elaborazione per il DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro [dell'enumerazione AEC \_ SYSTEM \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

La proprietà deve essere uno dei valori seguenti.



| Valore | Descrizione                                 |
|-------|---------------------------------------------|
| 0     | Modalità solo di annullamento dell'eco audio (AEC)     |
| 2     | Modalità solo elaborazione matrice microfono (MAP) |
| 4     | Modalità AEC e MAP                            |
| 5     | Né la modalità AEC né map                    |



 

È necessario impostare questa proprietà prima di usare il DSP di acquisizione vocale. Dopo aver impostato questa proprietà, è possibile usare il provider di servizi di configurazione con le impostazioni predefinite o impostare proprietà aggiuntive.

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

 

 
