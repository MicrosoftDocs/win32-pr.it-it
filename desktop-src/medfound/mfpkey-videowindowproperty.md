---
description: Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: Proprietà MFPKEY_VIDEOWINDOW (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527966"
---
# <a name="mfpkey_videowindow-property"></a>\_Proprietà VIDEOWINDOW di MFPKEY

Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCVideoWIndow

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

3000

## <a name="remarks"></a>Commenti

La finestra buffer è uno dei parametri del modello "leaky bucket" usato nel controllo della frequenza del codec.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Configurazione della codifica video](configuringvideoencoding.md)
</dt> <dt>

[Modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




