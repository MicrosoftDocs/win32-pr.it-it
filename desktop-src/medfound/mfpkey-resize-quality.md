---
description: Specifica se utilizzare un algoritmo che produce video di qualità superiore o un algoritmo più rapido.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Proprietà MFPKEY_RESIZE_QUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310599"
---
# <a name="mfpkey_resize_quality-property"></a>\_Proprietà ridimensiona \_ qualità MFPKEY

Specifica se utilizzare un algoritmo che produce video di qualità superiore o un algoritmo più rapido.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="applies-to"></a>Si applica a

-   [Ridimensionamento video DSP](videoresizer.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti:



| Valore     | Descrizione          |
|-----------|----------------------|
| VT \_ false | Algoritmo più veloce     |
| VT \_ true  | Video di qualità superiore |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
