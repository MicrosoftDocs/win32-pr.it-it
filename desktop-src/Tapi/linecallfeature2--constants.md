---
description: Le \_ costanti LINECALLFEATURE2 elencano le funzionalità aggiuntive disponibili per la conferenza, il trasferimento e le chiamate di parcheggio.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Costanti LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327883"
---
# <a name="linecallfeature2_-constants"></a>\_Costanti LINECALLFEATURE2

Le **costanti \_ LINECALLFEATURE2** elencano le funzionalità aggiuntive disponibili per la conferenza, il trasferimento e le chiamate di parcheggio.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**\_COMPLCALLBACK LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "callback" può essere richiamata usando l' \_ opzione di callback LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**\_COMPLCAMPON LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è attivato, la funzionalità "Camp on" può essere richiamata usando l'opzione LINECOMPLMODE di \_ campo con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**\_COMPLINTRUDE LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è attivato, la funzionalità "intrusione" può essere richiamata usando l' \_ opzione LINECOMPLMODE Intruder con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**\_COMPLMESSAGE LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è attivato, la funzionalità "lascia messaggio" può essere richiamata usando l' \_ opzione del messaggio LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**\_NOHOLDCONFERENCE LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è acceso, non è possibile creare una "conferenza di attesa" utilizzando l' \_ opzione LINECALLPARAMFLAGS NOHOLDCONFERENCE con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). Il \_ bit SETUPCONF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**\_ONESTEPTRANSFER LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è on, è possibile creare il "trasferimento di un passaggio" utilizzando l' \_ opzione LINECALLPARAMFLAGS ONESTEPTRANSFER con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Il \_ bit SETUPTRANSFER LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .

> [!Note]  
> Se nessuno dei bit "COMPl" viene specificato nel membro **dwCallFeatures2** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ viene specificato LINECALLFEATURE COMPLETECALL, è possibile che uno di essi funzionerà, ma il provider di servizi non ha specificato quale.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**\_TRANSFERCONF LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzione [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) può essere usata per risolvere il trasferimento come conferenza a tre vie. Il \_ bit COMPLETETRANSF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**\_TRANSFERNORM LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzione [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) può essere usata per risolvere il trasferimento come trasferimento normale. Il \_ bit COMPLETETRANSF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .

> [!Note]  
> Se non si specifica né TRANSFERNORM né TRANSFERCONF nel membro **dwCallFeatures2** di [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ viene specificato LINECALLFEATURE COMPLETETRANSF, è possibile che sia funzionante, ma che il provider di servizi non abbia specificato quale.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**\_PARKDIRECT LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è attivato, è possibile richiamare la funzionalità "directed Park" utilizzando l' \_ opzione LINEPARKMODE directed con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Il \_ bit del parco LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**\_PARKNONDIRECT LINECALLFEATURE2**
</dt> <dd> <dl> <dt>



Se questo bit è attivato, la funzionalità "parco non diretto" può essere richiamata usando l'opzione LINEPARKMODE non \_ indirizzata con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Il \_ bit del parco LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .

> [!Note]  
> Se non viene specificato né PARKDIRECT né PARKNONDIRECT nel membro **dwCallFeatures2** di [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ è stato specificato LINECALLFEATURE Park, è possibile che sia funzionante, ma che il provider di servizi non abbia specificato quale.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




