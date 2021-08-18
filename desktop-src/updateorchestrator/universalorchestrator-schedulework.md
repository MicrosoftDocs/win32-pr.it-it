---
title: IUniversalOrchestrator::ScheduleWork
description: Chiama Universal Orchestrator per pianificare il lavoro
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966086"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Metodo IUniversalOrchestrator::ScheduleWork

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

Consente ai client di informare Universal Orchestrator che il lavoro è in sospeso e di fornire un file binario che verrà chiamato da Universal Orchestrator per eseguire il lavoro di aggiornamento in un secondo momento.

Il file binario di callback deve essere firmato con un certificato Microsoft valido e il chiamante deve richiamare la chiamata ScheduleWork dal contesto SYSTEM.

## <a name="syntax"></a>Sintassi

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Parametri

`callerIdentifier`

Stringa univoca che identifica tutte le chiamate da questo client specifico.

`cmdLine`

Percorso completo del file binario di callback che verrà richiamato da Universal Orchestrator per eseguire operazioni.

`startArg`

Parametri da passare al file binario di callback per indicare che è richiesto Start.

`pauseArg`

*(facoltativo)* Parametri da passare al file binario di callback per indicare che è richiesta la sospensione.

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, **restituisce** S_OK .  In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



