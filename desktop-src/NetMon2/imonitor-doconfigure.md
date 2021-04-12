---
description: Il metodo DoConfigure deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere le informazioni di configurazione per l'acquisizione.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Metodo IMonitor::D oConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128915"
---
# <a name="imonitordoconfigure-method"></a>IMonitor::D Metodo oConfigure

Il metodo **DoConfigure** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere le informazioni di configurazione per l'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Nome di un'istanza del monitoraggio.

</dd> <dt>

*pConfiguration* \[ in\]
</dt> <dd>

Stringa di configurazione fornita da MCSVC. Il monitoraggio deve analizzare questa stringa per i dati di configurazione.

</dd> <dt>

*ppScriptInstance* \[ out\]
</dt> <dd>

Indirizzo della stringa HTML utilizzata per configurare il monitoraggio. Se per la configurazione viene utilizzato uno script predefinito, questo valore deve essere impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR) e MCSVC eseguirà il monitoraggio.

Se il metodo ha esito negativo, il valore restituito è un codice di errore. Il valore restituito di NMERR \_ Monitor \_ config \_ failed è accettabile, ma quando viene restituito questo errore non è possibile avviare il monitoraggio fino a quando non viene eseguita una futura chiamata **DoConfigure** . Qualsiasi altro errore impedisce l'attivazione dell'istanza del monitoraggio.

## <a name="remarks"></a>Commenti

MCSVC chiama questo metodo dopo che è stato connesso alla rete e prima che venga chiamato il metodo [IRTC:: Configure](irtc-configure.md) .

Il monitoraggio può archiviare le informazioni fornite da questa chiamata, aggiornare lo script HTML o la stringa di configurazione e impostare il [filtro di acquisizione](capture-filters.md) nel BLOB di NPP.

MCSVC può chiamare questo metodo più volte, ma non può essere chiamato durante l'acquisizione dei dati da parte del monitoraggio. Si noti che ogni volta che un [NPP](network-packet-providers.md) avvia un'acquisizione, la connessione alla rete deve essere configurata. Questa restrizione include le situazioni in cui il NPP inizia e arresta la stessa acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




