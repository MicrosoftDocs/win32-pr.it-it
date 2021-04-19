---
title: 'IUniversalOrchestrator:: scheduled'
description: Chiama l'agente di orchestrazione universale per pianificare il lavoro
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320074"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Metodo IUniversalOrchestrator:: Schedulement

> [!NOTE] 
> Questa API appartiene all'API dell'agente di orchestrazione universale.

Consente ai client di informare l'agente di orchestrazione universale che il lavoro è in sospeso e fornire un file binario che verrà chiamato dall'agente di orchestrazione universale per eseguire il lavoro di aggiornamento in un secondo momento.

Il file binario di callback deve essere firmato con un certificato Microsoft valido e il chiamante deve richiamare la chiamata pianificata dal contesto di sistema.

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

Percorso completo del file binario di callback che verrà richiamato dall'agente di orchestrazione universale per eseguire il lavoro.

`startArg`

Parametri da passare al file binario di callback per indicare che l'avvio è richiesto.

`pauseArg`

*(facoltativo)* Parametri da passare al file binario di callback per indicare che la pausa è richiesta.

## <a name="return-value"></a>Valore restituito
Se questo metodo ha esito positivo, restituisce **S_OK**.  In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |



 

 



