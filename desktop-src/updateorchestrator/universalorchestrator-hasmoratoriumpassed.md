---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Esegue una query dell'agente di orchestrazione universale per determinare se il periodo post-configurazione è stato superato.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320072"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>Metodo IUniversalOrchestrator:: HasMoratoriumPassed

> [!NOTE] 
> Questa API appartiene all'API dell'agente di orchestrazione universale.

Consente ai client di determinare se l'agente di orchestrazione universale funziona immediatamente dopo l'esperienza predefinita del nuovo dispositivo, il che limita i tentativi di lavoro per ridurre al minimo l'interruzione dell'utente. 

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

Parametro di output in cui è archiviato il risultato della query.

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



