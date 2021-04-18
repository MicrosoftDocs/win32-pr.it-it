---
description: Specifica se la complessità dell'algoritmo di codifica audio è vincolata.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Proprietà MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310649"
---
# <a name="mfpkey_constrainencomplexity-property"></a>\_Proprietà CONSTRAINENCOMPLEXITY di MFPKEY

Specifica se la complessità dell'algoritmo di codifica audio è vincolata.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore audio utilizza l'algoritmo predefinito. L'algoritmo predefinito dipende dal tipo di output e dalla versione di Windows in esecuzione. Nella tabella seguente viene descritto il comportamento predefinito per le diverse combinazioni.



| Sistema operativo | Comportamento predefinito                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Per tutti i tipi di output, per impostazione predefinita il codificatore audio utilizza l'algoritmo più complesso.                                                                                                                 |
| Windows 7        | Per i tipi di output standard e Professional, per impostazione predefinita il codificatore audio utilizza l'algoritmo più complesso. Per i tipi di output Lossless, per impostazione predefinita il codificatore audio utilizza l'algoritmo meno complesso. |



 

Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche un valore di complessità impostando la proprietà [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
