---
description: Imposta la modalità di elaborazione per il DSP di acquisizione voce.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Proprietà MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310265"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>\_ \_ Proprietà modalità di sistema WMAAECMA di MFPKEY \_

Imposta la modalità di elaborazione per il DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro dell'enumerazione [della \_ \_ modalità di sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

La proprietà deve essere uno dei valori seguenti.



| Valore | Descrizione                                 |
|-------|---------------------------------------------|
| 0     | Modalità di annullamento audio Echo (AEC)     |
| 2     | Modalità solo elaborazione array Microfoni (mappa) |
| 4     | Modalità AEC e MAP                            |
| 5     | Modalità AEC o MAP                    |



 

È necessario impostare questa proprietà prima di usare il DSP di acquisizione voce. Dopo aver impostato questa proprietà, è possibile usare il DSP con le impostazioni predefinite o impostare proprietà aggiuntive.

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

 

 
