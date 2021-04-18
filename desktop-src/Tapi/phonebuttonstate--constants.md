---
description: Le costanti del flag di bit PHONEBUTTONSTATE descrivono le posizioni dei pulsanti.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Costanti PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333953"
---
# <a name="phonebuttonstate_-constants"></a>Costanti PHONEBUTTONSTATE_

Le costanti del flag di bit **PHONEBUTTONSTATE_** descrivono le posizioni del pulsante.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Il pulsante si trova nello stato "giù" (premuto).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indica che lo stato verso l'alto o verso il basso del pulsante non è noto al provider di servizi e non verrà più conosciuto in un momento successivo. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indica che lo stato verso l'alto o verso il basso del pulsante non è noto in questo momento, ma può diventare noto in un momento successivo. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Il pulsante si trova nello stato "up".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sul telefono e non usare i valori PHONEBUTTONSTATE_ non supportati dalla versione negoziata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




