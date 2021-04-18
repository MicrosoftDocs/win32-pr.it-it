---
description: Le \_ costanti LINECALLPARAMFLAGS descrivono diversi flag di stato relativi a una chiamata.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Costanti LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324881"
---
# <a name="linecallparamflags_-constants"></a>\_Costanti LINECALLPARAMFLAGS

Le **costanti \_ LINECALLPARAMFLAGS** descrivono diversi flag di stato relativi a una chiamata.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**\_ID blocco LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



L'identità del mittente deve essere nascosta (ID chiamante del blocco).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**\_DESTOFFHOOK LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



Il telefono della parte chiamata dovrebbe essere Offhook automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inattivo**
</dt> <dd> <dl> <dt>



La chiamata deve essere originata su un aspetto di chiamata inattiva e non partecipare a una chiamata in corso. Quando si usa la funzione [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , se il \_ valore di inattività LINECALLPARAMFLAGS non è impostato ed è presente una chiamata esistente sulla riga, la funzione interrompe la chiamata esistente, se necessario, per eseguire la nuova chiamata. Se non è presente alcuna chiamata esistente, la funzione effettua la nuova chiamata come specificato.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**\_NOHOLDCONFERENCE LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



Questo bit viene usato solo in combinazione con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) e [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). L'indirizzo da usare per la conferenza con la chiamata corrente è specificato nel membro **targetAddress** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). La chiamata di consultazione non consente di creare fisicamente un tono di connessione dal commutino, ma passa attraverso diversi Stati di definizione della chiamata (ad esempio, la composizione, l'esecuzione). Quando la chiamata di consultazione raggiunge lo stato connesso, la conferenza viene stabilita automaticamente; la chiamata originale, che era rimasta nello stato connesso, entra nello stato di conferenza; la chiamata di consultazione entra nello stato di conferenza; il hConfCall entra nello stato connesso. Se la chiamata di consultazione ha esito negativo (entra nello stato disconnesso seguito da Idle), il hConfCall entra nello stato inattivo e la chiamata originale (che potrebbe essere stata una conferenza esistente, nel caso di **linePrepareAddToConference**) rimane nello stato connesso. L'entità o le parti originali non percepiscono mai che la chiamata è stata mantenuta. Questa funzionalità viene spesso usata per aggiungere un supervisore a una chiamata dell'agente ACD quando necessario per monitorare le interazioni con un chiamante irato.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**\_ONESTEPTRANSFER LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



Questo bit viene usato solo in combinazione con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Combina il funzionamento di **lineSetupTransfer** seguito da [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) nella chiamata di consultazione in un singolo passaggio. L'indirizzo da comporre viene specificato nel membro **targetAddress** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). La chiamata originale viene posizionata nello stato *onholdpendingtransfer* , come se **lineSetupTransfer** venisse chiamata normalmente e la chiamata di consultazione viene stabilita normalmente. L'applicazione deve comunque chiamare [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) per influire sul trasferimento. Questa funzionalità viene spesso utilizzata quando si richiama un trasferimento da un server tramite un collegamento di controllo delle chiamate di terze parti, perché tali collegamenti spesso non supportano il normale processo in due passaggi.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**\_ORIGOFFHOOK LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



Il telefono dell'originatore dovrebbe essere Offhook automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**\_PREDICTIVEDIAL LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



Questo bit viene usato solo quando si effettua una chiamata su un indirizzo con funzionalità di composizione predittiva (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER è on nel membro **DwAddrCapFlags** in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). Il bit deve essere attivato per abilitare l'avanzamento della chiamata avanzata e/o le funzionalità di monitoraggio dei dispositivi multimediali del dispositivo. Se questo bit non è impostato su on, la chiamata verrà effettuata senza lo stato di avanzamento della chiamata o il monitoraggio del tipo di supporto e non verrà avviato alcun trasferimento automatico in base allo stato di chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**\_sicurezza LINECALLPARAMFLAGS**
</dt> <dd> <dl> <dt>



La chiamata deve essere configurata come protetta.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




