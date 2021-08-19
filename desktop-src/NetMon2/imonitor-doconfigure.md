---
description: Il metodo DoConfigure deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere informazioni di configurazione per l'acquisizione.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Metodo IMonitor::D oConfigure (Netmon.h)
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
ms.openlocfilehash: 9776ca62cbb61b6708f00d5e1d6d85eeab245b32798683b5afde546d835633c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779191"
---
# <a name="imonitordoconfigure-method"></a>Metodo IMonitor::D oConfigure

Il **metodo DoConfigure** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere informazioni di configurazione per l'acquisizione.

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

*pName* \[ Pollici\]
</dt> <dd>

Nome di un'istanza del monitoraggio.

</dd> <dt>

*pConfiguration* \[ Pollici\]
</dt> <dd>

Stringa di configurazione fornita da MCSVC. Il monitoraggio deve analizzare questa stringa per i dati di configurazione.

</dd> <dt>

*ppScriptInstance* \[ Cambio\]
</dt> <dd>

Indirizzo della stringa HTML usata per configurare il monitoraggio. Se per la configurazione viene usato uno script predefinito, questo valore deve essere impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S OK (che corrisponde a \_ NOERROR) e MCSVC eseguirà il monitoraggio.

Se il metodo ha esito negativo, il valore restituito è un codice di errore. Un valore restituito di NMERR MONITOR CONFIG FAILED è accettabile, ma quando viene restituito questo errore, il monitoraggio non può essere avviato fino al completamento di una chiamata \_ \_ \_ **DoConfigure** futura. Qualsiasi altro errore impedisce l'a attivazione dell'istanza del monitoraggio.

## <a name="remarks"></a>Commenti

MCSVC chiama questo metodo dopo la connessione alla rete e prima che venga chiamato il metodo [IRTC::Configure.](irtc-configure.md)

Il monitoraggio può archiviare le informazioni fornite da questa chiamata, aggiornare lo script HTML o la stringa di configurazione e impostare il filtro [di acquisizione](capture-filters.md) nel BLOB NPP.

MCSVC può chiamare questo metodo più volte, ma non può essere chiamato durante l'acquisizione dei dati da parte del monitoraggio. Si noti che ogni volta [che un NPP](network-packet-providers.md) avvia un'acquisizione, è necessario configurare la connessione alla rete. Questa restrizione include le situazioni in cui NPP avvia e arresta la stessa acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




