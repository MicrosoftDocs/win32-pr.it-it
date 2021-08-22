---
description: Specifica la fine di un passaggio di codifica.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977c876d14c6757c5f1bc31e0d5b7cc58f6e13fad827cc23f821be8382a5e376
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738193"
---
# <a name="mfpkey_endofpass-property"></a>Proprietà MFPKEY \_ ENDOFPASS

Specifica la fine di un passaggio di codifica.

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo di dati per IPropertyBag

Non è necessario alcun tipo di dati. Per impostare questa proprietà, passare un elemento VARIANT non **inizializzato.**

## <a name="remarks"></a>Commenti

Questa proprietà non è una proprietà normale perché ha lo stesso effetto indipendentemente dal fatto che il valore sia VARIANT \_ TRUE o VARIANT \_ FALSE. È necessario impostare questa proprietà dopo aver elaborato gli ultimi esempi di input per un passaggio di pre-elaborazione. Se si eseguono più passaggi, è necessario impostare questa proprietà alla fine di ogni passaggio di pre-elaborazione (attualmente nessuno dei codec ne supporta più di uno). Se non si imposta questa proprietà, il codec presuppone che si stanno ancora passando esempi per la pre-elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




