---
description: Specifica un'altezza del frame intermedia per il video codificato.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Proprietà MFPKEY_FORCEFRAMEHEIGHT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227009"
---
# <a name="mfpkey_forceframeheight-property"></a>\_Proprietà FORCEFRAMEHEIGHT di MFPKEY

Specifica un'altezza del frame intermedia per il video codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile impostare questo valore e la [proprietà \_ FORCEFRAMEWIDTH di MFPKEY](mfpkey-forceframewidthproperty.md) per forzare il codificatore a codificare il flusso video con una dimensione del frame inferiore alle dimensioni del frame di input o di output. Una volta decodificato, il video verrà ridimensionato in base alla risoluzione di input originale.

Dimensioni del frame valide su entrambi gli assi sono da 2 a 8192 pixel. Le dimensioni del frame devono essere divisibili per 2.

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

 

 




