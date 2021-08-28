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
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625367"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



