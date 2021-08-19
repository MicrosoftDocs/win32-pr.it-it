---
description: Specifica il livello di alimentazione per il decodificatore.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874065"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>Proprietà MFPKEY \_ AVDecVideoSWPowerLevel

Specifica il livello di alimentazione per il decodificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**Interfaccia utente \_ VT4**

## <a name="default-value"></a>Valore predefinito

**100**

## <a name="remarks"></a>Commenti

Questa proprietà deve essere impostata su uno dei valori seguenti.



| Valore | Significato                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Il decodificatore usa un livello di alimentazione ottimizzato per la durata della batteria.  |
| 50    | Il decodificatore usa un livello di potenza bilanciato.                            |
| 100   | Il decodificatore usa un livello di alimentazione ottimizzato per la qualità video. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
