---
description: Specifica il numero medio di byte al secondo in un flusso audio in bit di variabile in base al livello di qualità (VBR).
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: Proprietà MFPKEY_WMAENC_AVGBYTESPERSEC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527955"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>MFPKEY \_ WMAENC- \_ Proprietà AVGBYTESPERSEC

Specifica il numero medio di byte al secondo in un flusso audio in bit di variabile in base al livello di qualità (VBR).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal decodificatore dopo la codifica del flusso.

Questo valore è richiesto dal decodificatore audio per decomprimere correttamente il contenuto.

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

 

 




