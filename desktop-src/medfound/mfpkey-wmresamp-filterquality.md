---
description: Specifica la qualità dell'output.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Proprietà MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226535"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>MFPKEY \_ WMRESAMP- \_ Proprietà FILTERQUALITY

Specifica la qualità dell'output.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="applies-to"></a>Si applica a

-   [DSP ricampionatore audio](audioresampler.md)

## <a name="remarks"></a>Commenti

L'intervallo valido di questa proprietà è compreso tra 1 e 60, inclusi. I valori più elevati producono un output di qualità superiore, ma introducono maggiore latenza. Il valore 1 è essenzialmente uguale all'interpolazione lineare.

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

 

 
