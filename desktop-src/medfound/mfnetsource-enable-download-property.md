---
description: Specifica se tutti i protocolli di download sono abilitati.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: MFNETSOURCE_ENABLE_DOWNLOAD proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7749dcdf15c099284a73cf6c55c1d753825230126e77a972e906b280a0b09a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738980"
---
# <a name="mfnetsource_enable_download-property"></a>Proprietà MFNETSOURCE \_ ENABLE \_ DOWNLOAD

Specifica se tutti i protocolli di download sono abilitati.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ ENABLE \_ DOWNLOAD** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** all'oggetto [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolli supportati](supported-protocols.md)
</dt> </dl>

 

 




