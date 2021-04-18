---
description: Le costanti del flag di bit PHONELAMPMODE descrivono i vari modi in cui è possibile accendere una lampada per telefoni.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: Costanti PHONELAMPMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8df5920df79e6fc59eb12bf1f517b4070e617d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333939"
---
# <a name="phonelampmode_-constants"></a>Costanti PHONELAMPMODE_

Le costanti dei flag di bit **PHONELAMPMODE_** descrivono i vari modi in cui è possibile illuminare una lampada del telefono.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Questo valore viene usato per descrivere una posizione di pulsante/lampada senza lampada corrispondente.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Flutter rotto è la superposizione di Flash e flutter.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash indica una riduzione del rallentamento.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Flutter significa fast on e off.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



La lampada è disattivata.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



Stabile indica che la lampada è accesa continuamente.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



La modalità lampada è attualmente sconosciuta.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Wink indica una frequenza normale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Dove le cadenza esatte possono variare in base a set di telefoni di fornitori diversi, il mapping dei modelli di illuminazione Lamp effettivi per la maggior parte dei telefoni sui valori elencati sopra dovrebbe essere semplice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




