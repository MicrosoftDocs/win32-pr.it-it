---
description: Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi. Lettura/scrittura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Proprietà MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324706"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>\_Proprietà CHECKDATACONSISTENCY2P di MFPKEY

Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi. Lettura/scrittura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ true**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **Variant \_ true**, il codificatore verifica che gli esempi di input corrispondano tra le due sessioni e non riesce se rileva una discrepanza. Lo scenario principale che causa una discrepanza consiste nel momento in cui l'input deriva da un dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
