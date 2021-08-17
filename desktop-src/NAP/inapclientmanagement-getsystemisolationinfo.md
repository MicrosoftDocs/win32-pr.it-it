---
title: Metodo INapClientManagement GetSystemIsolationInfo (NapManagement.h)
description: Recupera informazioni sullo stato di isolamento di NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Metodo GetSystemIsolationInfo nap
- Metodo GetSystemIsolationInfo NAP , interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414bb5f2d193aa8f7636b94925914afb7eb123d3b497fdc50d20498fa104fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368705"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>Metodo INapClientManagement::GetSystemIsolationInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetSystemIsolationInfo** recupera informazioni sullo stato di isolamento di NapClient.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene informazioni sullo stato di isolamento.

</dd> <dt>

*unknownConnections* \[ Cambio\]
</dt> <dd>

Puntatore a un flag che indica se una delle connessioni si trova in uno stato sconosciuto. In caso contrario, il flag viene impostato su **TRUE.** in caso contrario, il flag è impostato su **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, ma non solo, uno degli elementi seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>      | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

## <a name="remarks"></a>Commenti

Le informazioni di isolamento recuperate non riflettono stati sconosciuti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





