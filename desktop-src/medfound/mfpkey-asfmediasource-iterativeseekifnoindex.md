---
description: Configura l'origine dei supporti ASF in modo da usare la ricerca iterativa se il file di origine non ha un indice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761447"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>MFPKEY \_ ASFMediaSource- \_ Proprietà IterativeSeekIfNoIndex

Configura l'origine dei supporti ASF in modo da usare la ricerca iterativa se il file di origine non ha un indice.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine del supporto ASF. Per impostare la proprietà, passare un puntatore **IPropertyStore** al *resolver di origine*. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

La *ricerca iterativa* è un algoritmo per trovare una posizione in un file ASF senza indice. Usa una serie di approssimazioni, in base alla velocità in bit media, per avvicinarsi progressivamente al tempo di ricerca di destinazione. L'algoritmo è simile a una ricerca binaria. La ricerca iterativa può richiedere più tempo della ricerca in base all'indice, quindi è disabilitata per impostazione predefinita.

Se si imposta questa proprietà, utilizzare le proprietà seguenti per impostare i parametri di ricerca:

-   [Numero massimo di MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [\_ \_ Tolleranza ITERATIVESEEK ASFMediaSource \_ MFPKEY \_ in \_ millisecondi](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Queste proprietà impostano rispettivamente il numero massimo di iterazioni e la tolleranza. L'algoritmo si interrompe quando raggiunge il numero massimo di iterazioni oppure quando trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




