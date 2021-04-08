---
description: Specifica se la modalità Alpha per i tipi di video dei supporti colori è premoltiplicata o diritta.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Attributo MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050095"
---
# <a name="mf_mt_alpha_mode-attribute"></a>\_ \_ Attributo modalità MF mt Alpha \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Specifica se la modalità Alpha per i tipi di video dei supporti colori è premoltiplicata o diritta.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile eseguire il cast di questo valore in un valore in [**\_ \_ modalità DXGI Alpha**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) . Se questo attributo non è presente, per compatibilità con le versioni precedenti, il valore è **DXGI \_ Alpha \_ mode \_** per il formato video che supporta il canale alfa, ad esempio ARGB32, o **DXGI \_ Alpha \_ mode \_ Ignora** per il formato video senza canale alfa, ad esempio RGB32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
