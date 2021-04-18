---
description: Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Proprietà MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310626"
---
# <a name="mfpkey_loopfilter-property"></a>\_Proprietà LOOPFILTER di MFPKEY

Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="remarks"></a>Commenti

Il filtro in ciclo è un metodo di deblocco che viene applicato durante la codifica e la decodifica, per ridurre gli artefatti di blocco in fase di codifica ("nel ciclo"), in modo che i fotogrammi P futuri e i fotogrammi B non li portino avanti.

L'effetto dell'applicazione del filtro in ciclo è che i bordi dei blocchi macro nei fotogrammi video di output sono meno evidenti. Allo stesso tempo l'immagine può diventare più flessibile.

Sebbene il filtro in ciclo possa comportare una riduzione del dettaglio delle immagini in alcuni frame, la qualità complessiva del video trarrà vantaggio notevolmente. Lo svantaggio principale dell'uso del filtro in ciclo è il costo aggiuntivo per le prestazioni di decodifica.

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

 

 




