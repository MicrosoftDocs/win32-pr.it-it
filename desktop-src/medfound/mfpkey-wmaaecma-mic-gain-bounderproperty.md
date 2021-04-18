---
description: Specifica se l'acquisizione voce DSP applica la delimitazione del guadagno del microfono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Proprietà MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309119"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>\_Proprietà del \_ \_ limite Gain \_ MFPKEY WMAAECMA MIC

Specifica se l'acquisizione voce DSP applica la delimitazione del guadagno del microfono.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANT \_ true

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

La limitazione del guadagno del microfono garantisce che il livello di guadagno del microfono sia corretto. Se il guadagno è troppo elevato, il segnale acquisito potrebbe essere saturo e verrà ritagliato. Il ritaglio è un effetto non lineare, che causerà un errore dell'algoritmo di annullamento dell'eco acustico (AEC). Se il guadagno è troppo basso, il rapporto segnale/rumore è basso, che può anche causare un errore dell'algoritmo AEC o non funzionare correttamente.

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione                       |
|----------------|-----------------------------------|
| VARIANT \_ true  | Abilita delimitazione del guadagno del microfono.  |
| VARIANTE \_ false | Disabilitare la delimitazione del guadagno del microfono. |



 

Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled).

La limitazione del guadagno del microfono si applica solo quando il DSP funziona in modalità origine. In modalità filtro, l'applicazione deve verificare che il livello di guadagno del microfono sia corretto.

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

 

 
