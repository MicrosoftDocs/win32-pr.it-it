---
description: Rappresenta informazioni su un esperimento (acquisizione).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura dell'esperimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ebe9ab0232104886078256effdfaf5534144dc30421dab2ac2359ef390c0a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118151"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Struttura dell'esperimento

Rappresenta informazioni su un esperimento (acquisizione).

## <a name="syntax"></a>Sintassi


```C++
} Experiment;
```

## <a name="members"></a>Members

**Processid**  
ID del processo associato.

**applicationName**  
Stringa COM contenente il nome dell'applicazione in cui eseguire l'esperimento.

**commandLineArguments**  
Stringa COM contenente gli argomenti della riga di comando.

**Workingdirectory**  
Stringa COM contenente il percorso della directory di lavoro.

**tempPixRunFile**  
Stringa COM contenente il percorso del file temporaneo usato per eseguire l'esperimento.

**startOption**  
Opzione di avvio associata all'esperimento.

**experimentType**  
Tipo di esperimento (acquisizione).

**uiLocale**  
ID delle impostazioni locali usate per gli elementi di sovrimpressione dell'interfaccia utente durante l'esposizione (acquisizione). Viene passato dall'host (ad esempio, Visual Studio Diagnostica della grafica) al motore di acquisizione.

**registryRoot**  
Stringa COM contenente la radice del Registro di sistema. Viene passato dall'host (ad esempio, Visual Studio Diagnostica della grafica) al motore di acquisizione.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



