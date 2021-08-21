---
description: Le costanti LINECALLFEATURE2 elencano le funzionalità supplementari disponibili per le conferenze, il \_ trasferimento e le chiamate di parcheggio.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: LINECALLFEATURE2_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b1ef95c5427c70455466fdc4e44424a8d7bc92f768698bd3356f28256b4dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003139"
---
# <a name="linecallfeature2_-constants"></a>Costanti LINECALLFEATURE2 \_

Le **costanti LINECALLFEATURE2 \_** elencano le funzionalità supplementari disponibili per le conferenze, il trasferimento e le chiamate di parcheggio.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità di "callback" può essere richiamata usando l'opzione LINECOMPLMODE \_ CALLBACK con [**lineCompleteCall.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Anche il bit LINECALLFEATURE \_ COMPLETECALL sarà on nel **membro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "camp on" può essere richiamata usando l'opzione LINECOMPLMODE \_ CAMPON con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Anche il bit LINECALLFEATURE \_ COMPLETECALL sarà on nel **membro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "intrude" può essere richiamata usando l'opzione LINECOMPLMODE \_ INTRUDE con [**lineCompleteCall.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Anche il bit LINECALLFEATURE \_ COMPLETECALL sarà on nel **membro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "leave message" può essere richiamata usando l'opzione LINECOMPLMODE \_ MESSAGE con [**lineCompleteCall.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Anche il bit LINECALLFEATURE \_ COMPLETECALL sarà on nel **membro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Se questo bit è on, è possibile creare una "conferenza no hold" usando l'opzione LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). Anche il bit LINECALLFEATURE \_ SETUPCONF sarà on nel **membro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Se questo bit è on, è possibile creare un "trasferimento in un passaggio" usando l'opzione LINECALLPARAMFLAGS \_ ONESTEPTRANSFER con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Anche il bit LINECALLFEATURE \_ SETUPTRANSFER sarà on nel membro **dwCallFeatures.**

> [!Note]  
> Se nessuno dei bit "COMPL" è specificato nel membro **dwCallFeatures2** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma lineCALLFEATURE COMPLETECALL è specificato, è possibile che uno di essi funzioni, ma il provider di servizi non ha specificato \_ quale.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Se questo bit è on, è possibile usare la funzione [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) per risolvere il trasferimento come conferenza a tre livelli. Anche il bit LINECALLFEATURE \_ COMPLETETRANSF sarà on nel membro **dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Se questo bit è on, è possibile usare la [**funzione lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) per risolvere il trasferimento come trasferimento normale. Anche il bit LINECALLFEATURE \_ COMPLETETRANSF sarà on nel membro **dwCallFeatures.**

> [!Note]  
> Se né TRANSFERNORM né TRANSFERCONF vengono specificati nel membro **dwCallFeatures2** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma lineCALLFEATURE COMPLETETRANSF, è possibile che entrambi funzionino, ma il provider di servizi non ha specificato \_ quale.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "directed park" può essere richiamata usando l'opzione LINEPARKMODE \_ DIRECTED con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Anche il bit LINECALLFEATURE \_ PARK sarà on nel membro **dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Se questo bit è on, la funzionalità "non-directed park" può essere richiamata usando l'opzione LINEPARKMODE \_ NONDIRECTED con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Anche il bit LINECALLFEATURE \_ PARK sarà on nel membro **dwCallFeatures.**

> [!Note]  
> Se non vengono specificati NÉ PARKDIRECT né PARKNONDIRECT nel membro **dwCallFeatures2** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma LINECALLFEATURE PARK, è possibile che entrambi funzionino, ma il provider di servizi non ha specificato \_ quale.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



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

 

 




