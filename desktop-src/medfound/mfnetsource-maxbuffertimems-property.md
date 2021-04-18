---
description: Quantità massima di dati memorizzati nei buffer di origine della rete, in millisecondi.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Proprietà MFNETSOURCE_MAXBUFFERTIMEMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307961"
---
# <a name="mfnetsource_maxbuffertimems-property"></a>\_Proprietà MAXBUFFERTIMEMS di MFNETSOURCE

Quantità massima di dati memorizzati nei buffer di origine della rete, in millisecondi.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**DWORD** (archiviato come **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ MAXBUFFERTIMEMS** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore predefinito di questa proprietà è 40.000 millisecondi.

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

 

 




