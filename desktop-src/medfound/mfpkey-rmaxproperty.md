---
description: Specifica la velocità in bit del picco, in bit al secondo, usata per la riproduzione con frequenza in bit (VBR) a 2 passaggi vincolata.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Proprietà MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226977"
---
# <a name="mfpkey_rmax-property"></a>\_Proprietà Rmax di MFPKEY

Specifica la velocità in bit del picco, in bit al secondo, usata per la riproduzione con frequenza in bit (VBR) a 2 passaggi vincolata.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Nessuna impostazione predefinita.

## <a name="remarks"></a>Commenti

Questo valore rappresenta la velocità in bit massima per la riproduzione. Il valore di [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) viene usato per descrivere il buffer in base a questa velocità in bit. in effetti, il formato VBR vincolato è simile alla velocità in bit costante (CBR) che usa questo valore come velocità in bit. Tuttavia, un flusso VBR vincolato può essere riprodotto a una velocità in bit inferiore, a condizione che il buffer venga aumentato.

È necessario impostare questo valore per la codifica VBR a due passaggi con vincoli di picco. Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso. Il codificatore interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica. L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.

In genere, questo valore è da due a tre volte maggiore del valore di [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

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

 

 




