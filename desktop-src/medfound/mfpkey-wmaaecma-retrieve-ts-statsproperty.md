---
description: Specifica se il DSP di acquisizione vocale archivia le statistiche relative al timestamp nel registro di sistema.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Proprietà MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309115"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ - \_ recupero \_ proprietà statistiche Servizi terminal

Specifica se il DSP di acquisizione vocale archivia le statistiche relative al timestamp nel registro di sistema.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANTE \_ false

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Gli algoritmi AEC (Acoustic Echo Cancel) dipendono da timestamp accurati nei flussi audio. In realtà, i timestamp sono spesso imperfetti e diversi dispositivi audio possono presentare frequenze diverse di varianza e tendenza. Quando AEC è abilitato, il DSP raccoglie le statistiche relative ai timestamp e usa queste informazioni per compensare le imprecisioni.

Se il valore di questa proprietà è VARIANT \_ true, il DSP Salva le statistiche che raccoglie nel registro di sistema. La volta successiva che il DSP esegue l'AEC usando la stessa coppia di dispositivi audio, legge le informazioni statistiche dal registro di sistema, consentendo al DSP di eseguire in modo più efficiente.

Se si imposta il valore di questa proprietà su VARIANT \_ true e si usa il DSP in modalità filtro, è necessario impostare anche la proprietà [ \_ \_ \_ GUID MFPKEY WMAAECMA DEVICEPAIR](mfpkey-wmaaecma-devicepair-guidproperty.md) . In modalità origine questa operazione non è obbligatoria.

Il valore predefinito di questa proprietà è VARIANT \_ false. Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

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

 

 
