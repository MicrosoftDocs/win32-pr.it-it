---
description: Specifica la velocità in bit media, in bit al secondo, usata per la codifica a una velocità in bit (VBR) a 2 passaggi.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Proprietà MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310618"
---
# <a name="mfpkey_ravg-property"></a>\_Proprietà RAVG di MFPKEY

Specifica la velocità in bit media, in bit al secondo, usata per la codifica a una velocità in bit (VBR) a 2 passaggi.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

In un VBR vincolato e non vincolato, questo valore corrisponde alla velocità in bit media per tutta la durata del contenuto.

È necessario impostare questo valore per entrambe le modalità di codifica VBR a due passaggi. Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso. Il codificatore interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica. L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.

Questa proprietà può essere letta anche alla fine di una sessione di codifica VBR da 1 pass.

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

 

 




