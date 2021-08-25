---
description: Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi durante l'esecuzione della codifica VBR a due passaggi. Lettura/scrittura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cef9c8c2a8e4fcd536ce73653e80e62282b40734cc695493d6cba4187c8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954721"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>Proprietà MFPKEY \_ CHECKDATACONSISTENCY2P

Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi durante l'esecuzione della codifica VBR a due passaggi. Lettura/scrittura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ TRUE**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **VARIANT \_ TRUE,** il codificatore verifica che i campioni di input corrispondano tra i due passaggi e non riesce se rileva una discrepanza. Lo scenario principale che causa una discrepanza è quando l'input proviene da un dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
