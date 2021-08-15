---
description: Specifica se il codificatore principale usa il &\# 0034; Più&\# 0034; funzionalità.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab3fdcd3087773ea760615224b148bd497c1f89114c0f761a7d2f90fb0b5a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738018"
---
# <a name="mfpkey_enhanced_wma-property"></a>Proprietà \_ WMA AVANZATA MFPKEY \_

Specifica se il codificatore di base usa la funzionalità "Plus".

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**Interfaccia utente \_ VT4**

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile solo per Windows audio multimediale senza perdita.

Se si lascia questa proprietà sul valore predefinito 0 o se la si imposta su 1, il codificatore principale decide se usare la parte "Plus". Se si imposta questa proprietà su 2, il codificatore principale non usa la funzionalità "Plus".

Questa proprietà modifica i tipi di supporti enumerati, pertanto, se si imposta, è necessario farlo prima di impostare il tipo di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
