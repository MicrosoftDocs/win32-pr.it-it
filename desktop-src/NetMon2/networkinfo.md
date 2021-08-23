---
description: La struttura NETWORKINFO descrive una scheda di interfaccia di rete.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Struttura NETWORKINFO (Netmon.h)
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
ms.openlocfilehash: b5b57d7f051c1409c4b691d78d9173341efda984f35498289cd1eacb8c8b3199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555711"
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

Altro indirizzo che supporta questo (ad esempio IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Velocità del collegamento, in Mbps.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo di supporto.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Dimensioni massime del frame consentite.

</dd> <dt>

**Flag**
</dt> <dd>

Questo parametro può essere uno dei flag in informazioni seguenti:



| Valore                                                                                                                                                                                                                                       | Significato                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**FLAG NETWORKINFO \_ \_ PMODE \_ NON \_ SUPPORTATI**</dt> </dl>    | La scheda di rete non supporta la modalità promiscua, ovvero acquisisce solo il traffico trasmesso per natura o coinvolge solo il computer locale.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**NETWORKINFO \_ FLAG \_ RAS**</dt> </dl>                                                      | Si tratta di una scheda di rete virtuale che è una connessione RAS (Server di accesso remoto) tramite un modem o un'altra scheda di rete.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**SCHEDA REMOTA FLAG NETWORKINFO \_ \_ \_**</dt> </dl>                             | La scheda di rete non si trova nel computer locale, ma è in fase di acquisizione in un computer remoto al di fuori del computer locale.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ FLAG \_ REMOTE \_ NAL**</dt> </dl>                                | Obsoleto; non utilizzare .<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ FLAG \_ REMOTE \_ NAL \_ CONNECTED**</dt> </dl> | Obsoleto; non utilizzare .<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Ad esempio, il valore 1 indica 1/1 ms, 10 indica 1/10 ms, 100 indica 1/100 ms e così via.

</dd> <dt>

**Nodename**
</dt> <dd>

Nome della workstation remota.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicatore di supporto in modalità P nic.

</dd> <dt>

**Commento**
</dt> <dd>

Campo del commento dell'adapter.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




