---
description: Specifica il &\# 0034; bucket a perdita&\# 0034; parametri per un flusso in un sink multimediale ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Proprietà MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879598"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>MFPKEY \_ ASFSTREAMSINK- \_ correzione della \_ Proprietà LEAKYBUCKET

Specifica i parametri "leaky bucket" (vedere le note) per un flusso in un sink multimediale ASF.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Matrice di valori **DWORD** (**Caul**)

VT \_ vettore \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Commenti

Un'applicazione può impostare questa proprietà su un flusso del sink multimediale ASF dopo che è stato negoziato il tipo di supporto per il flusso. Utilizzare questa proprietà per specificare la finestra del buffer effettiva che verrà utilizzata dal codec Windows Media. È possibile ottenere queste informazioni dal codec usando l'interfaccia **IWMCodecLeakyBucket** , documentata in Windows Media Format SDK.

Il valore di questa proprietà è una matrice di tre valori **DWORD** nell'ordine seguente:

-   Velocità in bit, in bit al secondo.
-   Dimensioni del buffer, in byte.
-   Completezza del buffer iniziale, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




