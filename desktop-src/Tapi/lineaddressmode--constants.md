---
description: Le costanti del flag di bit LINEADDRESSMODE descrivono vari modi per \_ identificare un indirizzo in un dispositivo a linee.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4863b79c4527395f6ecb2d28c4d9ef718ff5a7fd99681185ba892bac2b4639ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761863"
---
# <a name="lineaddressmode_-constants"></a>Costanti \_ LINEADDRESSMODE

Le costanti del flag di bit **LINEADDRESSMODE \_** descrivono vari modi per identificare un indirizzo in un dispositivo a linee.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



L'indirizzo viene specificato con un numero intero piccolo compreso nell'intervallo da 0 a *dwNumAddresses* meno uno, dove *dwNumAddresses* è il valore nelle funzionalità del dispositivo della riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



L'indirizzo viene specificato tramite il relativo numero di telefono.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit meno bassi sono riservati.

Questa costante viene usata per selezionare un indirizzo in una riga da cui ha origine una chiamata. Il modello consueto seleziona l'indirizzo tramite il relativo identificatore di indirizzo. Gli identificatori di indirizzo sono il meccanismo usato per identificare gli indirizzi in TAPI. Tuttavia, in alcuni ambienti, quando si effettua una chiamata, è spesso più pratico identificare l'indirizzo di origine di una chiamata in base al numero di telefono anziché in base all'identificatore dell'indirizzo. Un esempio è la possibile modellazione di un numero elevato di stazioni (terze parti) sul commutatore tramite un dispositivo linea con molti indirizzi. La linea rappresenta il set di tutte le stazioni e ogni stazione è mappata a un indirizzo con il proprio numero di telefono principale e il proprio identificatore di indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




