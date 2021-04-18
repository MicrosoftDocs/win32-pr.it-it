---
description: Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, infrarossi o profondità.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Attributo MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309542"
---
# <a name="mf_mt_framesource_types-attribute"></a>\_ \_ Attributo origine frame di \_ tipo MF mt

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, infrarossi o profondità.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore deve essere un membro dell'enumerazione [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) . Per compatibilità con le versioni precedenti, quando questo attributo non è definito in un tipo di supporto, si presuppone che sia **\_ MFFrameSourceTyes:: color**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
