---
title: Struttura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contiene le informazioni di protezione accesso alla rete (NAP) su un supplicant EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Struttura EapHostPeerNapInfo EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048680"
---
# <a name="eaphostpeernapinfo-structure"></a>Struttura EapHostPeerNapInfo

La struttura **EapHostPeerNapInfo** contiene le informazioni di protezione accesso alla rete (NAP) su un supplicant EAP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Members

<dl> <dt>

**isolationState**
</dt> <dd>

Struttura [**di \_ stato di isolamento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) che specifica lo stato di isolamento NAP di un computer. Lo stato di isolamento determina il livello di accesso alla rete concesso.

</dd> <dt>

**probationTime**
</dt> <dd>

Struttura **ProbationTime** che specifica il tempo necessario affinché la connessione esca dalla quarantena dopo la quale viene eliminata la connessione. Una struttura **ProbationTime** è identica a una struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

Lunghezza, in byte, del [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) di protezione accesso alla rete che segue la struttura.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **EapHostPeerNapInfo** precede il [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) di protezione accesso alla rete del tipo di dati **WCHAR** nel flusso di byte RPC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                   |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Eaphostpeerapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture supplicant EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

