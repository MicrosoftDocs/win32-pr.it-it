---
description: Le \_ costanti del flag di bit LINEFORWARDMODE descrivono le condizioni in base alle quali è possibile inviare le chiamate a un indirizzo.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Costanti LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333548"
---
# <a name="lineforwardmode_-constants"></a>\_Costanti LINEFORWARDMODE

Le costanti del flag di bit **LINEFORWARDMODE \_** descrivono le condizioni in base alle quali è possibile inviare le chiamate a un indirizzo.

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ occupato**
</dt> <dd> <dl> <dt>



Fare in modo che tutte le chiamate siano occupate, indipendentemente dall'origine. Usare questo valore quando si esegue l'inoltri per le chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**\_BUSYEXTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Inviare tutte le chiamate esterne in occupato. Usare questo valore quando si esegue l'invio di chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**\_BUSYINTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate interne in occupato. Usare questo valore quando si esegue l'invio di chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**\_BUSYNA LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate su occupato/nessuna risposta, indipendentemente dall'origine. Usare questo valore quando si esegue l'inoltri per le chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**\_BUSYNAEXTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate esterne su occupato/nessuna risposta. Usare questo valore quando l'invio delle chiamate su occupato e su nessuna risposta non può essere controllato separatamente per le chiamate interne.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**\_BUSYNAINTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate interne su occupato/nessuna risposta. Usare questo valore quando l'invio delle chiamate su occupato e su nessuna risposta non può essere controllato separatamente per le chiamate interne.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**\_BUSYNASPECIFIC LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Avanti su occupato/nessuna risposta a tutte le chiamate originate a un indirizzo specificato (l'invio di chiamate selettive).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**\_BUSYSPECIFIC LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



In avanti, tutte le chiamate originate a un indirizzo specificato (invio di chiamate selettivo).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**\_NOANSW LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Inviare tutte le chiamate senza risposta, indipendentemente dall'origine. Utilizzare questo valore quando non è possibile controllare separatamente la chiamata di invio per chiamate interne ed esterne in nessuna risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**\_NOANSWEXTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate esterne senza risposta. Usare questo valore quando l'invio di chiamate interne ed esterne in nessuna risposta può essere controllato separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**\_NOANSWINTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate interne senza risposta. Usare questo valore quando l'invio di chiamate interne ed esterne in nessuna risposta può essere controllato separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**\_NOANSWSPECIFIC LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Avanti su nessuna risposta, tutte le chiamate originate a un indirizzo specificato (l'invio di chiamate selettivo).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE non \_ disponibile**
</dt> <dd> <dl> <dt>



Le chiamate vengono eseguite, ma le condizioni in cui si verificherà l'invio non sono note e non saranno mai note dal provider di servizi. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNcond**
</dt> <dd> <dl> <dt>



Inviare tutte le chiamate in modo incondizionato, indipendentemente dall'origine. Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne non può essere controllato separatamente. L'invio non condizionale esegue l'override in base alle condizioni di disponibilità e/o nessuna risposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**\_UNCONDEXTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Inviare tutte le chiamate esterne in modo incondizionato. Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne può essere controllato separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**\_UNCONDINTERNAL LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Invia tutte le chiamate interne in modo incondizionato. Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne può essere controllato separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**\_UNCONDSPECIFIC LINEFORWARDMODE**
</dt> <dd> <dl> <dt>



Inviare in modo non condizionale tutte le chiamate originate in corrispondenza di un indirizzo specificato, ovvero l'invio di una chiamata selettiva.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ sconosciuto**
</dt> <dd> <dl> <dt>



Le chiamate vengono eseguite, ma in questo momento non sono note le condizioni in cui si verificherà l'invio. È possibile che le condizioni possano diventare note in un momento successivo. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

I flag di bit definiti da LINEFORWARDMODE \_ non sono ortogonali. L'invio non condizionale ignora eventuali condizioni specifiche, ad esempio occupato o nessuna risposta. Se l'invio non condizionale non è attivo, l'invio su occupato e su nessuna risposta può essere controllato separatamente o non separatamente. Se controllato separatamente, i \_ flag LINEFORWARDMODE occupato e LINEFORWARDMODE \_ NOANSW possono essere usati separatamente. Se non è controllato separatamente, \_ è necessario usare il flag LINEFORWARDMODE BUSYNA. Analogamente, se l'invio di chiamate interne ed esterne può essere controllato separatamente, \_ \_ è possibile usare separatamente i flag esterni LINEFORWARDMODE interni e LINEFORWARDMODE; in caso contrario, viene usata la combinazione.

Le funzionalità degli indirizzi indicano quali modalità di invio sono disponibili per ogni indirizzo assegnato a una riga. Un'applicazione può usare [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) per impostare le condizioni di invio al passaggio.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questi \_ valori LINEFORWARDMODE se la versione negoziata non li supporta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




