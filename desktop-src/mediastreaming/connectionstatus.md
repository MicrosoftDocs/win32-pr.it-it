---
title: Enumerazione ConnectionStatus
description: Rappresenta lo stato del dispositivo nella rete come l'ultima volta.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API di streaming multimediale dell'enumerazione ConnectionStatus
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
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328370"
---
# <a name="connectionstatus-enumeration"></a>Enumerazione ConnectionStatus

Rappresenta lo stato del dispositivo nella rete come l'ultima volta.

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

Il dispositivo è online e attivo sulla rete.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**
</dt> <dd>

Il dispositivo è offline.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**In sospensione**
</dt> <dd>

Il dispositivo è attualmente offline ma potrebbe essere riattivato automaticamente quando viene effettuato un tentativo di comunicare con esso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt> </dl> |



 

 





