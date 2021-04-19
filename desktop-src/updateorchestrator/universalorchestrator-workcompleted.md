---
title: IUniversalOrchestrator::WorkCompleted
description: Chiama l'agente di orchestrazione universale per indicare che il lavoro è completato
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320075"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Metodo IUniversalOrchestrator:: WorkCompleted

> [!NOTE] 
> Questa API appartiene all'API dell'agente di orchestrazione universale.

Consente ai client di informare l'agente di orchestrazione universale che il lavoro pianificato in precedenza è stato completato e arrestare i callback per eseguire il lavoro fino alla successiva chiamata pianificata.

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

**True** se il lavoro è stato completato correttamente. In caso contrario, **false** se il tentativo di lavoro ha avuto esito negativo e deve essere ritentato in futuro. 

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



