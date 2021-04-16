---
description: Specifica una larghezza del frame intermedia per il video codificato.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Proprietà MFPKEY_FORCEFRAMEWIDTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528669"
---
# <a name="mfpkey_forceframewidth-property"></a>\_Proprietà FORCEFRAMEWIDTH di MFPKEY

Specifica una larghezza del frame intermedia per il video codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile impostare questo valore e la [proprietà \_ FORCEFRAMEHEIGHT di MFPKEY](mfpkey-forceframeheightproperty.md) per forzare il codificatore a codificare il flusso video con una dimensione del frame inferiore alle dimensioni del frame di input o di output. Una volta decodificato, il video verrà ridimensionato in base alla risoluzione di input originale.

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

 

 




