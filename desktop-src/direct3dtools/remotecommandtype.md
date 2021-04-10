---
description: Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione RemoteCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049036"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Enumerazione RemoteCommandType

Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**  
Avvia la comunicazione.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**  
Avvia una sessione di acquisizione Diagnostica della grafica (un esperimento).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**  
Avvia un'acquisizione (identica alla schermata di stampa). Inviato da un host durante l'acquisizione di un frame.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



