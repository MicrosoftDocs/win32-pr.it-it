---
description: Rappresenta le informazioni sul trigger dell'esperimento.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura ExperimentTrigger
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876441"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>Struttura ExperimentTrigger

Rappresenta le informazioni sul trigger dell'esperimento.

## <a name="syntax"></a>Sintassi


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Members

**type**  
Tipo di esperimento (acquisizione) attivato.

**key**  
Quando il tipo è uguale a EXPERIMENTTRIGGERTYPE:: KEY, la chiave usata per attivare l'acquisizione.

**NumeroFrame**  
Quando il tipo è uguale a EXPERIMENTTRIGGERTYPE:: NUMEROFRAME, il numero di frame che attiverà l'acquisizione.

**captureCount**  
Numero di frame sequenziali da acquisire.

**actionIID**  
ID dell'evento di azione (screenshot, acquisizione frame e così via).

**actionPlayload**  
Puntatore al payload dell'evento di azione.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



