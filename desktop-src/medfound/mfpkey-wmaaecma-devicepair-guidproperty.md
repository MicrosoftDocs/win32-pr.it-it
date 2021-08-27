---
description: Identifica la combinazione di dispositivi audio attualmente in uso dall'applicazione con il DSP di acquisizione vocale.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973330"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>Proprietà GUID DEL DISPOSITIVO MFPKEY \_ WMAAECMA \_ \_

Identifica la combinazione di dispositivi audio attualmente in uso dall'applicazione con il DSP di acquisizione vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ CLSID

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se si usa DSP in modalità filtro e il valore della proprietà [MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è VARIANT \_ TRUE.

Quando la proprietà [**MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è VARIANT TRUE, il DSP raccoglie le statistiche sui timestamp dai dispositivi audio e archivia queste informazioni nel Registro di \_ sistema. Queste statistiche possono cambiare per ogni combinazione di dispositivo di acquisizione audio e dispositivo di rendering audio. Pertanto, l'applicazione deve assegnare un GUID per identificare la combinazione specifica di dispositivi in uso. L'applicazione deve tenere traccia di questo GUID, in modo che possa assegnare lo stesso GUID ogni volta che usa la stessa coppia di dispositivi audio.

Se si usa il provider di servizi di configurazione in modalità di origine, non è necessario impostare questa proprietà. DSP genera automaticamente un GUID basato sul valore della proprietà [MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES.](mfpkey-wmaaecma-device-indexesproperty.md)

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

 

 
