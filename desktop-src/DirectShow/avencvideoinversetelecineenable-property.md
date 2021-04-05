---
description: Specifica se il codificatore esegue la telecine inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Proprietà AVEncVideoInverseTelecineEnable (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124995"
---
# <a name="avencvideoinversetelecineenable-property"></a>Proprietà AVEncVideoInverseTelecineEnable

Specifica se il codificatore esegue la telecine inversa.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoInverseTelecineEnable**

## <a name="remarks"></a>Commenti

Se il valore è **Variant \_ true**, il codificatore esegue la telecine inversa. Se non è necessaria la telecine inversa, impostare questa proprietà su **Variant \_ false**. Per eseguire la telecine inversa all'esterno del codificatore, impostare questa proprietà su **Variant \_ false** e impostare la proprietà [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) su eAVEncVideoOutputScan \_ SameAsInput.

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

 

 




