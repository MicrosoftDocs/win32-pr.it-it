---
description: Specifica la larghezza di banda della coppia di pacchetti e la larghezza di banda della fase di esecuzione rilevata dall'origine di rete.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Proprietà MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309533"
---
# <a name="mfnetsource_ppbandwidth-property"></a>\_Proprietà PPBANDWIDTH di MFNETSOURCE

Specifica la larghezza di banda della coppia di pacchetti e la larghezza di banda della fase di esecuzione rilevata dall'origine di rete. Il valore della proprietà è una matrice di due valori:

-   Larghezza di banda di coppie di pacchetti, in bit al secondo.
-   Larghezza di banda della fase di esecuzione, in bit al secondo.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Matrice di valori **ULONG** (**Caul**)

VT \_ vettore \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PPBANDWIDTH** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per recuperare questa proprietà, eseguire una query sull'origine di rete per l'interfaccia **IPropertyStore** e chiamare **IPropertyStore:: GetValue**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funzionalità di origine della rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




