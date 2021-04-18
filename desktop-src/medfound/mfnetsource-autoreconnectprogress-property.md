---
description: Il numero di volte che l'origine di rete ha tentato di riconnettersi alla rete.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Proprietà MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308408"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>\_Proprietà AUTORECONNECTPROGRESS di MFNETSOURCE

Il numero di volte che l'origine di rete ha tentato di riconnettersi alla rete.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**DWORD** (archiviato come **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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

 

 




