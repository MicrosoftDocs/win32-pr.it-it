---
description: Le \_ costanti del flag di bit LINEADDRESSMODE descrivono diversi modi per identificare un indirizzo in un dispositivo a linee.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Costanti LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328420"
---
# <a name="lineaddressmode_-constants"></a>\_Costanti LINEADDRESSMODE

Le costanti del flag di bit **LINEADDRESSMODE \_** descrivono diversi modi per identificare un indirizzo in un dispositivo a linee.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**\_ADDRESSID LINEADDRESSMODE**
</dt> <dd> <dl> <dt>



L'indirizzo viene specificato con un numero intero piccolo nell'intervallo compreso tra 0 e *dwNumAddresses* meno uno, dove *dwNumAddresses* è il valore nelle funzionalità del dispositivo della riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**\_DIALABLEADDR LINEADDRESSMODE**
</dt> <dd> <dl> <dt>



L'indirizzo viene specificato tramite il numero di telefono.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Questa costante viene utilizzata per selezionare un indirizzo su una riga in cui viene originata una chiamata. Il modello usuale seleziona l'indirizzo per mezzo del relativo identificatore di indirizzo. Gli identificatori di indirizzo sono il meccanismo usato per identificare gli indirizzi in TAPI. Tuttavia, in alcuni ambienti, quando si effettua una chiamata, è spesso più pratico identificare l'indirizzo di origine di una chiamata in base al numero di telefono anziché all'identificatore dell'indirizzo. Un esempio è la possibile modellazione di un numero elevato di stazioni (di terze parti) nel compartimento per mezzo di un dispositivo a linee con molti indirizzi. La riga rappresenta il set di tutte le stazioni e ogni stazione viene mappata a un indirizzo con il proprio numero di telefono primario e identificatore di indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




