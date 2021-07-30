---
title: IUniversalOrchestrator::ScheduleWork
description: Chiama Universal Orchestrator per pianificare il lavoro
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 4c49d06a28497c33e86cc1e919fdb59f2363d1f5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991818"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Metodo IUniversalOrchestrator::ScheduleWork

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

Consente ai client di informare Universal Orchestrator che il lavoro è in sospeso e di fornire un file binario che verrà chiamato da Universal Orchestrator per eseguire le operazioni di aggiornamento in un secondo momento.

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
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



