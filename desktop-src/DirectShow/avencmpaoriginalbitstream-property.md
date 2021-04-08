---
description: Specifica l'impostazione predefinita per il bit originale nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Proprietà AVEncMPAOriginalBitstream (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876774"
---
# <a name="avencmpaoriginalbitstream-property"></a>Proprietà AVEncMPAOriginalBitstream

Specifica l'impostazione predefinita per il bit originale nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può includere i valori seguenti.



| Valore          | Descrizione          |
|----------------|----------------------|
| VARIANTE \_ false | Il bit originale è disattivato. |
| VARIANT \_ true  | Il bit originale è on.  |



 

## <a name="remarks"></a>Commenti

Il codificatore potrebbe eseguire l'override di questa impostazione, in base al contenuto del flusso di input.

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

 

 




