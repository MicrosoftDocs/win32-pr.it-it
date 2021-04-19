---
description: Le \_ costanti LINEFEATURE elencano le operazioni che possono essere richiamate su una riga tramite questa API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Costanti LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333551"
---
# <a name="linefeature_-constants"></a>\_Costanti LINEFEATURE

Le **\_ costanti LINEFEATURE** elencano le operazioni che possono essere richiamate su una riga tramite questa API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**\_DEVSPECIFIC LINEFEATURE**
</dt> <dd> <dl> <dt>



È possibile usare le operazioni specifiche del dispositivo sulla riga.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**\_DEVSPECIFICFEAT LINEFEATURE**
</dt> <dd> <dl> <dt>



È possibile usare le funzionalità specifiche del dispositivo sulla riga.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ in futuro**
</dt> <dd> <dl> <dt>



L'invio di tutti gli indirizzi può essere usato sulla riga.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**\_FORWARDDND LINEFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con un indirizzo di destinazione vuoto) può essere usata per attivare la funzionalità non disturbare su tutti gli indirizzi sulla riga. \_Verrà impostato anche LINEFEATURE in futuro. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**\_FORWARDFWD LINEFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) può essere usata per inviare le chiamate su tutti gli indirizzi della riga ad altri numeri. \_Verrà impostato anche LINEFEATURE in futuro. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**\_MAKECALL LINEFEATURE**
</dt> <dd> <dl> <dt>



Una chiamata in uscita può essere inserita in questa riga usando un indirizzo non specificato.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**\_SETDEVSTATUS LINEFEATURE**
</dt> <dd> <dl> <dt>



La funzione [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) può essere richiamata sul dispositivo a linee. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**\_SETMEDIACONTROL LINEFEATURE**
</dt> <dd> <dl> <dt>



Il controllo multimediale può essere impostato su questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_**
</dt> <dd> <dl> <dt>



È possibile impostare le modalità Terminal per questa riga.

> [!Note]  
> Se nessuno dei nuovi bit "in" modificati è impostato nel membro **dwLineFeatures** in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) ma \_ viene impostato il bit di avanzamento LINEFEATURE, una qualsiasi delle modalità di avanzamento può funzionare. il provider di servizi non ha specificato semplicemente quelli.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Le \_ costanti LINEFEATURE vengono usate in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (restituite da [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)). [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) segnala, per una determinata riga, le funzionalità della linea che possono essere effettivamente richiamate mentre la riga si trova nello stato corrente. Un'applicazione rende questa determinazione dinamicamente dopo la modifica dello stato della riga, in genere causata dalle attività relative all'indirizzo o alla chiamata sulla riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




