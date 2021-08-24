---
title: Proprietà ITsSbClientConnection UserName
description: Recupera un valore che indica il nome dell'utente che ha avviato la connessione.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Proprietà UserName Servizi Desktop remoto, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto proprietà UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6961e6c911b24df2e6c3adbea14b31a2ce8e5a66a9be9082357db957e646a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511331"
---
# <a name="itssbclientconnectionusername-property"></a>Proprietà ITsSbClientConnection::UserName

Recupera un valore che indica il nome dell'utente che ha avviato la connessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un nome utente. Al termine dell'uso della stringa, liberarla chiamando la [**funzione SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

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

 

