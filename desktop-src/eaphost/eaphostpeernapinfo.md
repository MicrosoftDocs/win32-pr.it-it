---
title: Struttura EapHostPeerNapInfo (Eaphostpeerapis.h)
description: Contiene le informazioni di Protezione accesso alla rete (NAP) su un supplicant EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Struttura EAPHostPeerNapInfo
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
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274538"
---
# <a name="eaphostpeernapinfo-structure"></a>Struttura EapHostPeerNapInfo

La **struttura EapHostPeerNapInfo** contiene le informazioni di Protezione accesso alla rete in un supplicante EAP.

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

Struttura [**ISOLATION \_ STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) che specifica lo stato di isolamento protezione accesso alla rete di un computer. Lo stato di isolamento determina il livello di accesso alla rete concesso.

</dd> <dt>

**probationTime**
</dt> <dd>

Struttura **ProbationTime** che specifica il tempo necessario per uscire dalla quarantena della connessione dopo il quale la connessione verrà eliminata. Una **struttura ProbationTime** è identica a una [struttura FILETIME.](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

Lunghezza, in byte, della stringa [napCorrelationId](/windows/desktop/NAP/nap-datatypes) che segue questa struttura.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura EapHostPeerNapInfo** precede la stringa [NAPCorrelationId](/windows/desktop/NAP/nap-datatypes) del tipo di dati **WCHAR** nel flusso di byte RPC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Eaphostpeerapis.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture supplicant EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

