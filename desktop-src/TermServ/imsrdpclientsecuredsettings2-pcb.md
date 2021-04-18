---
title: Proprietà PCB IMsRdpClientSecuredSettings2
description: Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server. | Proprietà PCB IMsRdpClientSecuredSettings2
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientSecuredSettings2
- Interfaccia IMsRdpClientSecuredSettings2 Servizi Desktop remoto, proprietà PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321926"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a>IMsRdpClientSecuredSettings2::P la proprietà CB

Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a>Valore proprietà

Impostazione del PCB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





