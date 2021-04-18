---
description: Abilita la modalità a bassa latenza in un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Proprietà CODECAPI_AVLowLatencyMode (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305481"
---
# <a name="codecapi_avlowlatencymode-property"></a>Proprietà AVLowLatencyMode di codecapi \_

Abilita la modalità a bassa latenza in un codec.

## <a name="data-type"></a>Tipo di dati

**ULONG** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVLowLatencyMode**

## <a name="property-value"></a>Valore proprietà

Se il valore è diverso da zero, è abilitata la modalità a bassa latenza. Se il valore è zero, la modalità a bassa latenza è disabilitata.

## <a name="remarks"></a>Commenti

Questa proprietà si applica a codificatori e decodificatori.

La modalità a bassa latenza è utile per le comunicazioni in tempo reale o Live Capture, quando la latenza deve essere ridotta a icona. Tuttavia, la modalità a bassa latenza può ridurre anche la decodifica o la qualità della codifica.

Si prevede che il codificatore non aggiunga alcun ritardo di esempio a causa del riordino dei frame nel processo di codifica e un esempio di input produrrà un esempio di output. Le sezioni e i frame B possono essere presenti a condizione che non introducano un nuovo ordinamento del frame nel codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

