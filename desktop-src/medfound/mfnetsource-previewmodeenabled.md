---
description: Abilita o Disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica di buffer iniziale.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Proprietà MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315009"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>\_Proprietà PREVIEWMODEENABLED di MFNETSOURCE

Abilita o Disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica di buffer iniziale.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**BOOL**

\_bool VT

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PREVIEWMODEENABLED** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Questa proprietà viene impostata nell'origine di rete passando un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




