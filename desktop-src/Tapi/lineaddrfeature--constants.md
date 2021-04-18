---
description: Le \_ costanti LINEADDRFEATURE elencano le operazioni che possono essere richiamate su un indirizzo.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Costanti LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328314"
---
# <a name="lineaddrfeature_-constants"></a>\_Costanti LINEADDRFEATURE

Le **costanti \_ LINEADDRFEATURE** elencano le operazioni che possono essere richiamate su un indirizzo.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ in futuro**
</dt> <dd> <dl> <dt>



L'indirizzo può essere inviato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**\_MAKECALL LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



È possibile inserire una chiamata in uscita sull'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE \_ pickup**
</dt> <dd> <dl> <dt>



È possibile prelevare una chiamata all'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**\_PICKUPDIRECT LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per prelevare una chiamata su un indirizzo specifico.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**\_PICKUPGROUP LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per selezionare una chiamata nel gruppo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**\_PICKUPHELD LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **null** ) può essere usata per selezionare una chiamata mantenuta sull'indirizzo. Questa operazione viene in genere usata solo in una disposizione con bridging esclusivo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**\_PICKUPWAITING LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **null** ) può essere usata per selezionare una chiamata in attesa. Si noti che questo non indica necessariamente che è effettivamente presente una chiamata in attesa, perché spesso è impossibile per un dispositivo di telefonia rilevare automaticamente tale chiamata; viene tuttavia indicato che la funzione hook-Flash verrà richiamata per tentare di passare a una chiamata di questo tipo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**\_SETMEDIACONTROL LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



Il controllo multimediale può essere impostato su questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



È possibile impostare le modalità Terminal per questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**\_SETUPCONF LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



A questo indirizzo è possibile configurare una chiamata di conferenza con una chiamata iniziale **null** .


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**\_UNCOMPLETECALL LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



Le richieste di completamento delle chiamate possono essere annullate a questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNpark**
</dt> <dd> <dl> <dt>



È possibile deparcheggiare le chiamate usando questo indirizzo.

> [!Note]  
> Se nessuno dei nuovi bit "PICKUP" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma \_ è impostato il bit di prelievo LINEADDRFEATURE, è possibile che una qualsiasi delle modalità di prelievo funzioni. il provider di servizi non ha specificato semplicemente quelli.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**\_FORWARDDND LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con un indirizzo di destinazione vuoto) può essere usata per attivare la funzionalità non disturbare sull'indirizzo. \_Verrà impostato anche LINEADDRFEATURE in futuro.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**\_FORWARDFWD LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) può essere usata per inviare chiamate sull'indirizzo ad altri numeri. \_Verrà impostato anche LINEADDRFEATURE in futuro.

> [!Note]  
> Se nessuno dei nuovi bit "in" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma \_ viene impostato il bit di avanzamento LINEADDRFEATURE, è possibile che una qualsiasi delle modalità di avanzamento funzioni. il provider di servizi non ha specificato semplicemente quelli.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Questa costante viene usata sia in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (restituito da [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) che in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (restituito da [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **LINEADDRESSCAPS** segnala la disponibilità delle funzionalità degli indirizzi da parte del provider di servizi (principalmente il Commuti) per un determinato indirizzo. Un'applicazione determina questa decisione quando Inizializza. La struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) segnala, per un determinato indirizzo, le funzionalità che possono essere effettivamente richiamate mentre l'indirizzo si trova nello stato corrente. Un'applicazione rende questa determinazione dinamicamente dopo le modifiche dello stato dell'indirizzo, in genere dovute alle attività relative alle chiamate sull'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




