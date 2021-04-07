---
description: Rappresenta le informazioni su un esperimento (acquisizione).
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
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746442"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Struttura dell'esperimento

Rappresenta le informazioni su un esperimento (acquisizione).

## <a name="syntax"></a>Sintassi


```C++
} Experiment;
```

## <a name="members"></a>Members

**processId**  
ID del processo associato.

**applicationName**  
Stringa COM contenente il nome dell'applicazione in cui eseguire l'esperimento.

**commandLineArguments**  
Stringa COM contenente gli argomenti della riga di comando.

**workingDirectory**  
Stringa COM contenente il percorso della directory di lavoro.

**tempPixRunFile**  
Stringa COM contenente il FilePath del file temporaneo usato per eseguire l'esperimento.

**startOption**  
Opzione di avvio associata all'esperimento.

**experimentType**  
Tipo di esperimento (acquisizione).

**uiLocale**  
ID delle impostazioni locali utilizzate per gli elementi di sovrapposizione dell'interfaccia utente durante il experiement (acquisizione). Viene passato dall'host (ad esempio Visual Studio Diagnostica della grafica) al motore di acquisizione.

**registryRoot**  
Stringa COM contenente la radice del registro di sistema. Viene passato dall'host (ad esempio Visual Studio Diagnostica della grafica) al motore di acquisizione.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



