---
description: Arresta il passaggio di codifica corrente o esegue una query se il passaggio di codifica corrente è l'ultimo.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Proprietà AVEncCommonPassEnd (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482516"
---
# <a name="avenccommonpassend-property"></a>Proprietà AVEncCommonPassEnd

Arresta il passaggio di codifica corrente o esegue una query se il passaggio di codifica corrente è l'ultimo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Commenti

L'impostazione di questa proprietà su **Variant \_ true** termina il passaggio di codifica corrente. Se si imposta questa proprietà su **Variant \_ false** , viene terminata la codifica Multipass.

La lettura di questa proprietà esegue una query se il passaggio di codifica corrente è l'ultimo.

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

 

 




