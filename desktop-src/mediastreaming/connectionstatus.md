---
title: Enumerazione ConnectionStatus
description: Rappresenta lo stato del dispositivo nella rete come visualizzato per l'ultima volta.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- Api Streaming multimediale dell'enumerazione ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721251"
---
# <a name="connectionstatus-enumeration"></a>Enumerazione ConnectionStatus

Rappresenta lo stato del dispositivo nella rete come visualizzato per l'ultima volta.

## <a name="syntax"></a>Sintassi


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**
</dt> <dd>

Il dispositivo è online e attivo nella rete.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**
</dt> <dd>

Il dispositivo è offline.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Dormire**
</dt> <dd>

Il dispositivo è attualmente offline, ma potrebbe essere riattivato automaticamente quando viene effettuato un tentativo di comunicare con esso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (riferimento Windows. Media.Streaming.idl)</dt> </dl> |



 

 





