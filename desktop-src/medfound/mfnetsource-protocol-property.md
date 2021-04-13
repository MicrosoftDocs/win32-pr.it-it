---
description: Specifica il protocollo di controllo utilizzato dall'origine di rete.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: Proprietà MFNETSOURCE_PROTOCOL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525980"
---
# <a name="mfnetsource_protocol-property"></a>\_Proprietà del protocollo MFNETSOURCE

Specifica il protocollo di controllo utilizzato dall'origine di rete. Il valore di questa proprietà è un membro dell'enumerazione [**del \_ \_ tipo di protocollo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

Il **\_ protocollo Constant MFNETSOURCE** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolli supportati](supported-protocols.md)
</dt> </dl>

 

 




