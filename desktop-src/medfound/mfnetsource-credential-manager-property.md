---
description: Contiene un puntatore all'interfaccia IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Proprietà MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130115"
---
# <a name="mfnetsource_credential_manager-property"></a>\_Proprietà di \_ Gestione credenziali MFNETSOURCE

Contiene un puntatore all'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Usare questa proprietà per passare l'implementazione dell'applicazione di [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) all'origine di rete.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Puntatore **IUnknown**

VT \_ sconosciuto

**punkVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ Credential \_ Manager** definisce il **GUID** per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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

[Autenticazione origine rete](network-source-authentication.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




