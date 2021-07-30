---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Esegue una query su Universal Orchestrator per determinare se il periodo post-OOBE è stato superato.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 3ccbf673b8fe22fabe7001112e04e87bd45eeaa4
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991798"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>Metodo IUniversalOrchestrator::HasMoratoriumPassed

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

Consente ai client di determinare se Universal Orchestrator funziona immediatamente dopo il nuovo dispositivo Out of Box Experience, che limita i tentativi di lavoro per ridurre al minimo l'interruzione dell'utente. 

## <a name="syntax"></a>Sintassi

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parametri

`callerIdentifier`

Stringa univoca che identifica tutte le chiamate da questo client specifico.

`hasMoratoriumPassed`

Parametro di output che archivia il risultato della query.

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



