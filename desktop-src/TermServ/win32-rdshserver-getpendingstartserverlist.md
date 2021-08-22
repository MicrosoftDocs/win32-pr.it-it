---
title: Metodo GetPendingStartServerList della Win32_RDSHServer classe
description: Recupera un elenco di server in attesa di avvio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Metodo GetPendingStartServerList Servizi Desktop remoto
- Metodo GetPendingStartServerList Servizi Desktop remoto , Win32_RDSHServer classe
- Win32_RDSHServer classe Servizi Desktop remoto metodo , GetPendingStartServerList
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
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422651"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Metodo GetPendingStartServerList della classe RDSHServer Win32 \_

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

*maxServers* \[ Pollici\]
</dt> <dd>

Numero massimo di server da restituire nell'elenco.

</dd> <dt>

*ServerFQDN* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, contiene una raccolta di nomi di dominio completi dei server in attesa di avvio.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'elenco dei server viene reimpostato dopo ogni chiamata, in modo che la chiamata successiva non otterrà un server duplicato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ cimv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





