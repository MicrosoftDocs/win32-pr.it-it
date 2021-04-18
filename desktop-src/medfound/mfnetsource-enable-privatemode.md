---
description: Abilita la modalità di download privata nell'origine di rete.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Proprietà MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308402"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ Abilita \_ Proprietà PRIVATEMODE

Abilita la modalità di download privata nell'origine di rete.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**BOOL**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

Se questa proprietà è **true**, la cache viene cancellata al termine della sessione.

La costante **MFNETSOURCE \_ CLIENTGUID** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




