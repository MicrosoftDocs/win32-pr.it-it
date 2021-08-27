---
description: La costante del flag di bit LINETRANSLATEOPTION \_ descrive un'opzione usata dalla conversione degli indirizzi.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: LINETRANSLATEOPTION_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d1cc9f3d7798dda9dd5bb69817ccfac64ae88fbc45fccccd59563cc24614d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073021"
---
# <a name="linetranslateoption_-constants"></a>Costanti LINETRANSLATEOPTION \_

La costante del flag di bit **LINETRANSLATEOPTION \_** descrive un'opzione usata dalla conversione degli indirizzi.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



Se per la posizione è definita una stringa Cancel Call Waiting, l'impostazione di questo bit comporterà l'inserimento della stringa all'inizio della stringa dialable. Viene comunemente usato dalle applicazioni modem e fax per evitare l'interruzione delle chiamate da parte dei besp in attesa di chiamata. Se per la posizione non è definita alcuna stringa Cancel Call Waiting, questo bit non ha alcun effetto. Si noti che si consiglia alle applicazioni che usano questo bit di impostare anche il bit LINECALLPARAMFLAGS SECURE nel membro \_ **dwCallParamFlags** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passato a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) tramite il parametro *lpCallParams,* in modo che se il dispositivo a linee usa un meccanismo diverso dalle cifre dialable per eliminare gli interrupt di chiamata, verrà richiamato tale meccanismo.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



La scheda chiamante predefinita deve essere sostituita con una specificata.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



Questa opzione forza la traduzione dell'indirizzo (numero) come long distance.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



Questa opzione forza la traduzione del numero (indirizzo) come locale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




