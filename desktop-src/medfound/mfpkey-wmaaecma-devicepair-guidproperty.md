---
description: Identifica la combinazione di dispositivi audio che l'applicazione sta attualmente usando con il DSP di acquisizione voce.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Proprietà MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130546"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>\_ \_ Proprietà GUID MFPKEY WMAAECMA DEVICEPAIR \_

Identifica la combinazione di dispositivi audio che l'applicazione sta attualmente usando con il DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_CLSID VT

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se si utilizza il DSP in modalità filtro e il valore della proprietà [MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è Variant \_ true.

Quando la proprietà [**MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è la variante \_ true, il DSP raccoglie le statistiche relative ai timestamp dai dispositivi audio e archivia tali informazioni nel registro di sistema. Queste statistiche possono cambiare per ogni combinazione di dispositivo di acquisizione audio e dispositivo di rendering audio. Pertanto, l'applicazione deve assegnare un GUID per identificare la combinazione specifica di dispositivi in uso. L'applicazione deve tenere traccia di questo GUID, in modo che possa assegnare lo stesso GUID ogni volta che usa la stessa coppia di dispositivi audio.

Se si usa il DSP in modalità origine, non è necessario impostare questa proprietà. Il DSP genera automaticamente un GUID basato sul valore della proprietà [MFPKEY \_ WMAAECMA \_ Device \_ indexes](mfpkey-wmaaecma-device-indexesproperty.md) .

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

 

 
