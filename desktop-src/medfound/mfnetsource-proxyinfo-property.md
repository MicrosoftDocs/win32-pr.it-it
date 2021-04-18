---
description: Archivia il nome host e la porta del server proxy utilizzato dall'origine di rete.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Proprietà MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314024"
---
# <a name="mfnetsource_proxyinfo-property"></a>\_Proprietà PROXYINFO di MFNETSOURCE

Archivia il nome host e la porta del server proxy utilizzato dall'origine di rete.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

\_LPWSTR VT

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYINFO** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per ottenere il valore della proprietà dall'origine di rete, chiamare **IPropertyStore:: GetValue** e passare la struttura **PropertyKey** nel parametro *Key* . Il membro **fmtid** di **PropertyKey** deve essere impostato sul GUID della proprietà.

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

[Supporto del proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




