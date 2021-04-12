---
description: Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Proprietà MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226539"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>MFPKEY \_ WMADEC- \_ Proprietà DRCMODE

Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACDRCSetting

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questo valore integer è compreso tra 0 e 2. Maggiore è il valore, minore è l'intervallo dinamico dell'output audio non compresso. Il valore 0 indica che il codec non esegue alcun controllo di intervallo dinamico, ovvero il codec non modifica l'intervallo dinamico intrinseco del contenuto codificato.

Se questo valore è impostato su 1 o 2, il codec utilizzerà le proprietà seguenti per determinare il controllo intervallo dinamico necessario:

-   [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)
-   [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)

Se non si specificano valori di destinazione, il codec fornirà un proprio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




