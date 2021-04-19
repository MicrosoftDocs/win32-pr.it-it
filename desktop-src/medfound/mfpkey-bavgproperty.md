---
description: Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit media (specificata da MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Proprietà MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311589"
---
# <a name="mfpkey_bavg-property"></a>\_Proprietà BAVG di MFPKEY

Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit media (specificata da [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCBAvg

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Nessun valore predefinito, ma il codec calcolerà un valore appropriato in base alle altre impostazioni VBR vincolate.

## <a name="remarks"></a>Commenti

Questo valore viene calcolato dal codec dopo il passaggio di codifica finale. Non eseguire una query per questo valore fino al completamento della codifica. Il codec interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica; L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.

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

 

 




