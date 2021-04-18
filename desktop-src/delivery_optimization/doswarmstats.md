---
title: Struttura DOSwarmStats (Deliveryoptimization. h)
description: Contiene i campi per scaricare e caricare le statistiche per un file.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Struttura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302658"
---
# <a name="doswarmstats-structure"></a>Struttura DOSwarmStats

Contiene i campi per scaricare e caricare le statistiche per un file.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Members

<dl> <dt>

**fileId**
</dt> <dd>

Stringa con terminazione null specificata con la chiamata **AddFileWithRanges** .

</dd> <dt>

**sourceURL**
</dt> <dd>

Stringa con terminazione null che contiene il nome del file nel server, ad esempio il percorso del &lt; server https:// &gt; / &lt; &gt; /file.ext.

</dd> <dt>

**fileSize**
</dt> <dd>

Dimensioni del file, in byte.

</dd> <dt>

**totalBytesDownloaded**
</dt> <dd>

Numero totale di byte trasferiti.

</dd> <dt>

**bytesFromLanPeers**
</dt> <dd>

Numero di byte trasferiti dai peer LAN.

</dd> <dt>

**bytesFromGroupPeers**
</dt> <dd>

Numero di byte trasferiti da peer di gruppo.

</dd> <dt>

**bytesFromInternetPeers**
</dt> <dd>

Numero di byte trasferiti dai peer internet.

</dd> <dt>

**bytesFromHttp**
</dt> <dd>

Numero di byte trasferiti da http.

</dd> <dt>

**bytesFromDoinc**
</dt> <dd>

Solo per uso interno.

</dd> <dt>

**bytesToLanPeers**
</dt> <dd>

Numero di byte trasferiti ai peer LAN.

</dd> <dt>

**bytesToGroupPeers**
</dt> <dd>

Numero di byte trasferiti ai peer di gruppo.

</dd> <dt>

**bytesToInternetPeers**
</dt> <dd>

Numero di byte trasferiti ai peer internet.

</dd> <dt>

**httpConnectionCount**
</dt> <dd>

Numero di connessioni HTTP.

</dd> <dt>

**doincConnectionCount**
</dt> <dd>

Solo per uso interno.

</dd> <dt>

**lanConnectionCount**
</dt> <dd>

Conteggio delle connessioni LAN.

</dd> <dt>

**groupConnectionCount**
</dt> <dd>

Conteggio delle connessioni al gruppo.

</dd> <dt>

**internetConnectionCount**
</dt> <dd>

Conteggio delle connessioni Internet.

</dd> <dt>

**downloadDuration**
</dt> <dd>

Durata del trasferimento di file in millisecondi.

</dd> <dt>

**Modalità**
</dt> <dd>

Per la modalità di download usata, vedere [**modalità**](downloadmode.md).

</dd> <dt>

**Stato**
</dt> <dd>

Lo stato di un trasferimento di file, vedere [**SwarmStatus**](swarmstatus.md).

</dd> <dt>

**isBackground**
</dt> <dd>

True se si tratta di un trasferimento in background.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





