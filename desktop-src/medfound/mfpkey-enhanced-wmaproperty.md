---
description: Specifica se il codificatore principale usa il &\# 0034; Più&\# 0034; funzionalità.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Proprietà MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333535"
---
# <a name="mfpkey_enhanced_wma-property"></a>\_ \_ Proprietà WMA avanzata MFPKEY

Specifica se il codificatore principale utilizza la funzionalità "più".

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile solo per Windows Media Audio Lossless.

Se si lascia questa proprietà sul valore predefinito 0 oppure se si imposta su 1, il codificatore Core decide se utilizzare la parte "più". Se si imposta questa proprietà su 2, il codificatore principale non userà la funzionalità "Plus".

Questa proprietà modifica i tipi di supporto enumerati, pertanto se si imposta è necessario eseguire questa operazione prima di impostare il tipo di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
