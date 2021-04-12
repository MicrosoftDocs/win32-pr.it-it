---
title: Metodo GetPendingStartServerList della classe Win32_RDSHServer
description: Recupera un elenco di server in attesa di avvio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetPendingStartServerList
- Metodo GetPendingStartServerList Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400673"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Metodo GetPendingStartServerList della \_ classe RDSHServer Win32

Recupera un elenco di server in attesa di avvio.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maxServers* \[ in\]
</dt> <dd>

Numero massimo di server da restituire nell'elenco.

</dd> <dt>

*ServerFQDNs* \[ out\]
</dt> <dd>

Se l'operazione ha esito positivo, contiene una raccolta di nomi di dominio completi dei server in attesa di avvio.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'elenco dei server viene reimpostato dopo ogni chiamata, in modo che la chiamata successiva non otterrà un server duplicato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





