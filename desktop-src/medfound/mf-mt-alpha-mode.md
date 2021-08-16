---
description: Specifica se la modalità alfa per i tipi di video multimediali a colori è premoltimulata o retta.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c658cae64c68aa89c49230164707d75369c021767c6aa0b46818516ffa26513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035319"
---
# <a name="mf_mt_alpha_mode-attribute"></a>Attributo \_ MF MT \_ ALPHA \_ MODE

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Specifica se la modalità alfa per i tipi di video multimediali a colori è premoltimulata o retta.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile eseguire il cast di questo valore a un [**valore DXGI \_ ALPHA \_ MODE.**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) Se questo attributo non è presente, per compatibilità con le versioni precedenti, il valore è **DXGI \_ ALPHA \_ MODE \_ STRAIGHT** per il formato video che supporta il canale alfa, ad esempio ARGB32 o **DXGI \_ ALPHA MODE \_ \_ IGNORE** per il formato video senza canale alfa, ad esempio RGB32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
