---
description: Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da MFPKEY \_ Rmax).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Proprietà MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318403"
---
# <a name="mfpkey_bmax-property"></a>\_Proprietà BMAX di MFPKEY

Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCBMax

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Nessuna impostazione predefinita.

## <a name="remarks"></a>Commenti

È necessario impostare questo valore per la codifica VBR con vincoli di picco. Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso. Il codec interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica; L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.

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

 

 




