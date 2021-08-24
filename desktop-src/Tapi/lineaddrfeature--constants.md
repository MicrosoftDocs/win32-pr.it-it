---
description: Le costanti LINEADDRFEATURE elencano le operazioni che \_ possono essere richiamate su un indirizzo.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: LINEADDRFEATURE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bb545bdf0195d9fd8ed35833150b9cfd1f6b10bfbd3d1ead7e8ebff65c93132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682220"
---
# <a name="lineaddrfeature_-constants"></a>Costanti LINEADDRFEATURE \_

Le **costanti LINEADDRFEATURE \_** elencano le operazioni che possono essere richiamate su un indirizzo.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ FORWARD**
</dt> <dd> <dl> <dt>



L'indirizzo può essere inoltrato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Una chiamata in uscita può essere inserita nell'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**RITIRO LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



Una chiamata può essere prelevata all'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



La [**funzione linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per prelevare una chiamata su un indirizzo specifico.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



La [**funzione linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per prelevare una chiamata nel gruppo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**
</dt> <dd> <dl> <dt>



La [**funzione linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **Null)** può essere usata per prelevare una chiamata che viene mantenuta sull'indirizzo. In genere viene usato solo in una disposizione esclusiva con bridge.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



La [**funzione linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **Null)** può essere usata per prelevare una chiamata in attesa di chiamata. Si noti che ciò non indica necessariamente che una chiamata in attesa è effettivamente presente, perché spesso non è possibile che un dispositivo di telefonia rilevi automaticamente tale chiamata; indica tuttavia che la funzione hook-flash verrà richiamata per tentare di passare a tale chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Il controllo dei supporti può essere impostato su questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINALE**
</dt> <dd> <dl> <dt>



È possibile impostare le modalità terminale per questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



A questo indirizzo è possibile configurare una **conferenza** telefonica con una chiamata iniziale NULL.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



Le richieste di completamento delle chiamate possono essere annullate a questo indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNPARK**
</dt> <dd> <dl> <dt>



Le chiamate possono essere scollegate usando questo indirizzo.

> [!Note]  
> Se nessuno dei nuovi bit "PICKUP" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma il bit LINEADDRFEATURE PICKUP è impostato, è possibile che una delle modalità di ritiro funzioni. Il provider di servizi non ha semplicemente specificato \_ quali.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La [**funzione lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con un indirizzo di destinazione vuoto) può essere usata per attivare la funzionalità Non disturbare sull'indirizzo. Verrà impostata anche LINEADDRFEATURE \_ FORWARD.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La [**funzione lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) può essere usata per inoltrare chiamate sull'indirizzo ad altri numeri. Verrà impostata anche LINEADDRFEATURE \_ FORWARD.

> [!Note]  
> Se nessuno dei nuovi bit "FORWARD" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma il bit LINEADDRFEATURE FORWARD è impostato, è possibile che una delle modalità di inoltro funzioni. Il provider di servizi non ha semplicemente specificato \_ quali.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Questa costante viene usata sia in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (restituito da [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) che in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (restituito da [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **LINEADDRESSCAPS indica** la disponibilità delle funzionalità degli indirizzi da parte del provider di servizi (principalmente l'opzione ) per un determinato indirizzo. Un'applicazione determina questa determinazione quando viene inizializzata. La [**struttura LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) segnala, per un determinato indirizzo, quali funzionalità di indirizzo possono essere effettivamente richiamate mentre l'indirizzo è nello stato corrente. Un'applicazione effettua questa determinazione in modo dinamico dopo le modifiche dello stato dell'indirizzo, in genere causate da attività correlate alle chiamate nell'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



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

 

 




