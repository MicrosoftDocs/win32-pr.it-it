---
description: Specifica una rappresentazione numerica del compromesso tra la fluidità del movimento e la qualità dell'immagine dell'output del codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Proprietà MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755487"
---
# <a name="mfpkey_crisp-property"></a>MFPKEY ( \_ Proprietà croccante)

Specifica una rappresentazione numerica del compromesso tra la fluidità del movimento e la qualità dell'immagine dell'output del codec.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

75

## <a name="remarks"></a>Commenti

Questo valore integer può variare da 0 a 100. Maggiore è il valore, maggiore sarà il codec per ottimizzare la codifica per la qualità dell'immagine dei singoli frame, che in genere riduce la fluidità del movimento.

Questa proprietà deve essere impostata solo per la codifica di velocità in bit costante (CBR). Le ottimizzazioni per la codifica con velocità in bit variabile (VBR) funzionano in modo diverso.

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

 

 




