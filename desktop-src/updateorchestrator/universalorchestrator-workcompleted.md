---
title: IUniversalOrchestrator::WorkCompleted
description: Chiama Universal Orchestrator per indicare che il lavoro è stato completato
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991828"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Metodo IUniversalOrchestrator::WorkCompleted

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

Consente ai client di informare Universal Orchestrator che il lavoro pianificato in precedenza è stato completato e di arrestare i callback per l'esecuzione del lavoro fino alla successiva chiamata ScheduleWork riuscita.

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



 

 



