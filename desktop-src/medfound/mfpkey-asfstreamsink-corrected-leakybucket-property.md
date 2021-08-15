---
description: Specifica i parametri &\# 0034;leaky bucket&0034; per un flusso in un sink multimediale \# ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb41de92f160e3d73c7d15721dae3015efc0ad1bc1a982d1a22c542d311b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874081"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET - proprietà

Specifica i parametri "leaky bucket" (vedere la sezione Osservazioni) per un flusso in un sink multimediale ASF.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Matrice di **valori DWORD** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**Caul**



## <a name="remarks"></a>Commenti

Un'applicazione può impostare questa proprietà su un flusso del sink multimediale di ASF dopo che il tipo di supporto per il flusso è stato negoziato. Usare questa proprietà per specificare la finestra del buffer effettiva che verrà Windows codec multimediale. È possibile ottenere queste informazioni dal codec usando l'interfaccia **IWMCodecLeakyBucket,** documentata in Windows Media Format SDK.

Il valore di questa proprietà è una matrice di tre **valori DWORD** nell'ordine seguente:

-   Velocità in bit, in bit al secondo.
-   Dimensioni del buffer, in byte.
-   Completezza iniziale del buffer, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




