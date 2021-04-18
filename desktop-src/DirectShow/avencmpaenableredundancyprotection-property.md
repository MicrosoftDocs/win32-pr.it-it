---
description: Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Proprietà AVEncMPAEnableRedundancyProtection (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304148"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Proprietà AVEncMPAEnableRedundancyProtection

Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione                |
|----------------|----------------------------|
| VARIANTE \_ false | Non aggiungere un checksum CRC. |
| VARIANT \_ true  | Aggiungere un checksum CRC.        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




