---
title: IUniversalOrchestrator::WorkCompleted
description: Chiama Universal Orchestrator per indicare che il lavoro è stato completato
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966075"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Metodo IUniversalOrchestrator::WorkCompleted

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

Consente ai client di informare Universal Orchestrator che il lavoro pianificato in precedenza è stato completato e di arrestare i callback per eseguire il lavoro fino alla successiva chiamata scheduleWork riuscita.

## <a name="syntax"></a>Sintassi

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parametri

`callerIdentifier`

Stringa univoca che identifica tutte le chiamate da questo client specifico.

`workCompleted`

**TRUE** se il lavoro è stato completato correttamente. In caso **contrario, FALSE** se il tentativo di lavoro non è riuscito e deve essere ritentato in futuro. 

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



