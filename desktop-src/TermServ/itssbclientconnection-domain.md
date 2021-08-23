---
title: Proprietà di dominio ITsSbClientConnection
description: Recupera un valore che indica il nome di dominio del client Connessione Desktop remoto (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Proprietà di dominio Servizi Desktop remoto
- Proprietà di dominio Servizi Desktop remoto, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto , proprietà Domain
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc99724eb419e831e65f402299aa1603be07ab2ab5a88e0ba9b056492514865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511511"
---
# <a name="itssbclientconnectiondomain-property"></a>Proprietà ITsSbClientConnection::D omain

Recupera un valore che indica il nome di dominio del client Connessione Desktop remoto (RDC).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una **variabile BSTR** che contiene il nome di dominio del client RdC. Al termine dell'uso della stringa, liberarla chiamando la [**funzione SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

