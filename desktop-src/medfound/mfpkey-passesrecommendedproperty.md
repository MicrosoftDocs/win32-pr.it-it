---
description: Specifica il numero massimo di passaggi supportati dal codificatore.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Proprietà MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226999"
---
# <a name="mfpkey_passesrecommended-property"></a>\_Proprietà PASSESRECOMMENDED di MFPKEY

Specifica il numero massimo di passaggi supportati dal codificatore. Di sola lettura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere il valore di questa proprietà chiamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Se si usa **IPropertyBag**, è innanzitutto necessario impostare il valore fourcc del formato compresso desiderato usando la proprietà [MFPKEY \_ fourcc](mfpkey-fourccproperty.md) .

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

 

 




