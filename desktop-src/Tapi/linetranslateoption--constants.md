---
description: La \_ costante del flag di bit LINETRANSLATEOPTION descrive un'opzione utilizzata dalla conversione degli indirizzi.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Costanti LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327496"
---
# <a name="linetranslateoption_-constants"></a>\_Costanti LINETRANSLATEOPTION

La costante del flag di bit **LINETRANSLATEOPTION \_** descrive un'opzione utilizzata dalla conversione degli indirizzi.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**\_CANCELCALLWAITING LINETRANSLATEOPTION**
</dt> <dd> <dl> <dt>



Se per la posizione è definita una stringa di attesa di chiamata Cancel, l'impostazione di questo bit provocherà l'inserimento di tale stringa all'inizio della stringa di connessione. Questa operazione viene in genere utilizzata dal modem dati e dalle applicazioni fax per evitare interruzioni di chiamate dai segnali acustici in attesa. Se per la posizione non è definita alcuna stringa di attesa di chiamata Cancel, questo bit non ha alcun effetto. Si noti che per le applicazioni che usano questo bit è consigliabile impostare anche il \_ bit sicuro LINECALLPARAMFLAGS nel membro **dwCallParamFlags** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) tramite il parametro *lpCallParams* , in modo che, se il dispositivo della linea usa un meccanismo diverso dalle cifre che è possibile comporre per impedire l'interruzione della chiamata, il meccanismo verrà richiamato.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**\_CARDOVERRIDE LINETRANSLATEOPTION**
</dt> <dd> <dl> <dt>



È necessario eseguire l'override della scheda chiamante predefinita con una specifica.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**\_FORCELD LINETRANSLATEOPTION**
</dt> <dd> <dl> <dt>



Questa opzione impone che l'indirizzo (numero) venga convertito come Long distance.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**\_FORCELOCAL LINETRANSLATEOPTION**
</dt> <dd> <dl> <dt>



Questa opzione impone al numero (indirizzo) di essere convertito come locale.


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

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




