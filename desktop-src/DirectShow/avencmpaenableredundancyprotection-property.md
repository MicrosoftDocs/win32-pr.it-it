---
description: Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Proprietà AVEncMPAEnableRedundancyProtection (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b50e010b0b088e8817eca4dae1989cd6f623f55a9616c4449df62f115f98ff7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824111"
---
# <a name="avencmpaenableredundancyprotection-property"></a>AVEncMPAEnableRedundancyProtection - proprietà

Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione                |
|----------------|----------------------------|
| VARIANT \_ FALSE | Non aggiungere un checksum CRC. |
| VARIANT \_ TRUE  | Aggiungere un checksum CRC.        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




