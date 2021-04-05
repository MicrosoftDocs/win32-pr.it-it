---
title: Metodo INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso di NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- NAP metodo GetSystemIsolationInfoEx
- Metodo GetSystemIsolationInfoEx NAP, interfaccia INapClientManagement2
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
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048162"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Metodo INapClientManagement2:: GetSystemIsolationInfoEx

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetSystemIsolationInfoEx** recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso di NapClient.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene informazioni sullo stato di isolamento.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Puntatore a un BOOL che è **true** se una delle connessioni è in uno stato sconosciuto e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

## <a name="remarks"></a>Commenti

Le informazioni di isolamento recuperate non riflettono gli stati sconosciuti.

SHA deve liberare la struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





