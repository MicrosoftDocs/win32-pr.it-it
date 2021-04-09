---
description: Specifica se il contenuto viene memorizzato nella cache dell'origine di rete.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Proprietà MFNETSOURCE_CACHEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879806"
---
# <a name="mfnetsource_cacheenabled-property"></a>\_Proprietà CACHEENABLED di MFNETSOURCE

Specifica se il contenuto viene memorizzato nella cache dell'origine di rete.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Booleano (**Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ CACHEENABLED** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore predefinito di questa proprietà è **true**.

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

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




