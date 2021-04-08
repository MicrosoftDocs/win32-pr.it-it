---
description: La struttura NETWORKINFO descrive una scheda di interfaccia di rete.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Struttura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760130"
---
# <a name="networkinfo-structure"></a>Struttura NETWORKINFO

La struttura NETWORKINFO descrive una scheda di interfaccia di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**PermanentAddr**
</dt> <dd>

Indirizzo MAC permanente.

</dd> <dt>

**CurrentAddr**
</dt> <dd>

Indirizzo MAC corrente.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Altro indirizzo che supporta questa operazione (ad esempio, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Velocità di collegamento, in Mbps.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo di supporto.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Dimensione massima consentita per il frame.

</dd> <dt>

**Flag**
</dt> <dd>

Questo parametro può essere uno dei seguenti flag informativi:



| Valore                                                                                                                                                                                                                                       | Significato                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_flag NETWORKINFO \_ pmode \_ non \_ supportati**</dt> </dl>    | La scheda di rete non supporta la modalità promiscua, ovvero acquisisce solo il traffico trasmesso in natura o solo il computer locale.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**\_RAS flag \_ NETWORKINFO**</dt> </dl>                                                      | Si tratta di una scheda di rete virtuale che è una connessione RAS (server di accesso remoto) tramite un modem o un'altra scheda di rete.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**\_ \_ scheda remota flag \_ NETWORKINFO**</dt> </dl>                             | La scheda di rete non si trova nel computer locale, ma viene acquisita in un computer remoto con il lascio del computer locale.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ flag \_ \_ NAL remoto**</dt> </dl>                                | Obsoleto Non usare.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ flags \_ Remote \_ NAL \_ Connected**</dt> </dl> | Obsoleto Non usare.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Ad esempio, il valore 1 indica 1/1 MS, 10 indica 1/10 ms, 100 indica 1/100 ms e così via.

</dd> <dt>

**NodeName**
</dt> <dd>

Nome della workstation remota.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicatore di supporto della modalità P NIC.

</dd> <dt>

**Commento**
</dt> <dd>

Campo di commento dell'adapter.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




