---
description: Valore che indica se un frame è stato acquisito usando l'illuminazione a infrarossi attivi (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Attributo MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307977"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>\_ \_ \_ Attributo per l'illuminazione del frame di metadati di acquisizione MF \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che indica se un frame è stato acquisito usando l'illuminazione a infrarossi attivi (IR).

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo è una maschera di maschera. Si tratta di un valore a 64 bit per la compatibilità con le versioni precedenti.

L'illuminazione attiva si verifica quando un dispositivo ha un emettitore chiaro vicino alla fotocamera IR che emette un fascio di luce per illuminare la scena, in genere emette luce IR in modo che non disturbi gli occhi umani. Impostare Value su (value & 0x1)! = 0 se frame è stato acquisito quando l'illuminazione attiva era impostata su on e set (value & 0x1) = = 0 se l'illuminazione attiva è disattivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




