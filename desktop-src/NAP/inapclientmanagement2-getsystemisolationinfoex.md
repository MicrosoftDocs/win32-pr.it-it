---
title: Metodo INapClientManagement2 GetSystemIsolationInfoEx (NapManagement.h)
description: Recupera informazioni sullo stato di isolamento e lo stato di isolamento esteso di NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Metodo GetSystemIsolationInfoEx nap
- Metodo GetSystemIsolationInfoEx NAP , interfaccia INapClientManagement2
- Interfaccia INapClientManagement2 NAP, metodo GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03630cbd0647dc177460f92abc28e6aa66cbb663465ba7e9e93eefbc283ac00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621928"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Metodo INapClientManagement2::GetSystemIsolationInfoEx

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetSystemIsolationInfoEx** recupera informazioni sullo stato di isolamento e lo stato di isolamento esteso di NapClient.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene informazioni sullo stato di isolamento.

</dd> <dt>

*unknownConnections* \[ Cambio\]
</dt> <dd>

Puntatore a un oggetto BOOL **che è TRUE** se una delle connessioni si trova in uno stato sconosciuto e FALSE in caso **contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, ma non solo, uno degli elementi seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>      | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

## <a name="remarks"></a>Commenti

Le informazioni di isolamento recuperate non riflettono stati sconosciuti.

L'SHA deve liberare la [**struttura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

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

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





