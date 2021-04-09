---
description: Specifica la fine di un passaggio di codifica.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Proprietà MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880806"
---
# <a name="mfpkey_endofpass-property"></a>\_Proprietà ENDOFPASS di MFPKEY

Specifica la fine di un passaggio di codifica.

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo di dati per IPropertyBag

Nessun tipo di dati richiesto. Per impostare questa proprietà, passare una **variante** non inizializzata.

## <a name="remarks"></a>Commenti

Questa proprietà non è una proprietà normale perché ha lo stesso effetto indipendentemente dal fatto che il valore sia VARIANT \_ true o Variant \_ false. È necessario impostare questa proprietà dopo l'elaborazione degli ultimi esempi di input per un passaggio di pre-elaborazione. Se si eseguono più sessioni, è necessario impostare questa proprietà alla fine di ogni passaggio di pre-elaborazione (al momento nessuno dei codec supporta più di uno). Se non si imposta questa proprietà, il codec presuppone che si stiano ancora passando esempi per la pre-elaborazione.

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

 

 




