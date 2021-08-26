---
description: Le costanti del flag di bit PHONEBUTTONSTATE descrivono le posizioni dei pulsanti.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: PHONEBUTTONSTATE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95070eb24b5189b44f07a8ba2d2d7ed7d8234ec14a97889f09c0fe29ac72eed9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100510"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ costanti

Le **PHONEBUTTONSTATE_** flag di bit descrivono le posizioni del pulsante.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Il pulsante si trova nello stato "down" (premuto).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indica che lo stato verso l'alto o verso il basso del pulsante non è noto al provider di servizi e non diventerà noto in un momento futuro. (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indica che lo stato verso l'alto o verso il basso del pulsante non è noto in questo momento, ma potrebbe diventare noto in un momento futuro. (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Il pulsante si trova nello stato "su".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Per la compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sul telefono e non usare i valori PHONEBUTTONSTATE_ non supportati dalla versione negoziata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




