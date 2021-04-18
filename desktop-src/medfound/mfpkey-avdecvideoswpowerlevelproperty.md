---
description: Specifica il livello di alimentazione per il decodificatore.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Proprietà MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307955"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>\_Proprietà AVDecVideoSWPowerLevel di MFPKEY

Specifica il livello di alimentazione per il decodificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="default-value"></a>Valore predefinito

**100**

## <a name="remarks"></a>Commenti

Questa proprietà deve essere impostata su uno dei valori seguenti.



| Valore | Significato                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Il decodificatore usa un livello di alimentazione ottimizzato per la durata della batteria.  |
| 50    | Il decodificatore usa un livello di risparmio energia bilanciato.                            |
| 100   | Il decodificatore usa un livello di alimentazione ottimizzato per la qualità del video. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
