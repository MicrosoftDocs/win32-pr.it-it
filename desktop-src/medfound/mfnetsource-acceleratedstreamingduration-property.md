---
description: Durata del flusso accelerato per l'origine di rete, in millisecondi.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Proprietà MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879810"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>\_Proprietà ACCELERATEDSTREAMINGDURATION di MFNETSOURCE

Durata del flusso accelerato per l'origine di rete, in millisecondi.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**DWORD** (archiviato come **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un oggetto **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica alla funzionalità di avvio rapido di servizi Windows Media, che riproduce rapidamente il contenuto senza attendere la lunga memorizzazione nella memoria iniziale. Quando si utilizza avvio rapido, il server che esegue Windows Media Services invierà alcuni dati all'inizio del contenuto a una velocità più elevata rispetto a quella specificata dalla velocità in bit del contenuto.

Il valore predefinito di questa proprietà è 10.000 millisecondi.

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

 

 




