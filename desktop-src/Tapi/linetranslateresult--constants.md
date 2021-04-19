---
description: Le \_ costanti del flag di bit LINETRANSLATERESULT descrivono i vari risultati di una conversione degli indirizzi.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Costanti LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333544"
---
# <a name="linetranslateresult_-constants"></a>\_Costanti LINETRANSLATERESULT

Le costanti del flag di bit **LINETRANSLATERESULT \_** descrivono i vari risultati di una conversione degli indirizzi.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ canonico**
</dt> <dd> <dl> <dt>



Indica che la stringa di input è in formato canonico valido.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**\_DIALBILLING LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene un valore "$".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**\_DIALDIALTONE LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene un "W".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**\_DIALPROMPT LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene un "?".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**\_DIALQUIET LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene "@".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ internazionale**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata internazionale (il codice paese o regione specificato nell'indirizzo di destinazione è diverso dal codice paese o regione specificato per il **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INtoll**
</dt> <dd> <dl> <dt>



Indica che la chiamata locale viene comunicata come Long Distance perché il paese o l'area geografica ha una chiamata a pedaggio e il prefisso viene visualizzato nel **TollPrefixList** di **CurrentLocation**.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ locale**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata locale (il codice del paese o dell'area geografica e il prefisso specificato nell'indirizzo di destinazione sono uguali a quelli specificati per **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**\_LONGDISTANCE LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata a distanza estesa (il codice paese o regione specificato nell'indirizzo di destinazione è lo stesso, ma il codice di area è diverso da quelli specificati per **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**\_NOTINTOLLLIST LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che il paese o l'area geografica supporta la chiamata a pedaggio, ma il prefisso non viene visualizzato in **TollPrefixList**, quindi la chiamata viene chiamata come chiamata locale. Si noti che se sia l'intollo che NOTINTOLLIST sono disattivati, il paese o l'area geografica corrente non supporta i prefissi di pedaggio e gli elementi dell'interfaccia utente correlati ai prefissi di pedaggio non devono essere presentati all'utente. Se uno dei due bit è attivato, il paese o l'area geografica supporta elenchi a pedaggio e gli elementi dell'interfaccia utente correlati devono essere abilitati.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**NOTRANSLATION LINETRANSLATERESULT \_**
</dt> <dd> <dl> <dt>



Indica che la conversione degli indirizzi non è disponibile. Questo elemento è esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**\_VOICEDETECT LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo di connessione restituito contiene ":". Questo elemento è esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.

> [!Note]  
> Il carattere ":" (due punti) verrà aggiunto all'elenco di caratteri che possono essere incorporati in una stringa di connessione e passati agli indirizzi di destinazione. Il tentativo di passare da un'applicazione a un dispositivo a linee che supporta una versione API precedente alla 2,0 genererà probabilmente LINEERR \_ INVALADDRESS o eventualmente nel carattere ignorato completamente. Il significato di questo carattere è "Sospendi fino a quando non viene rilevata una richiesta vocale, quindi continua la composizione"; viene usato per la connessione automatica a sistemi che forniscono richieste vocali, ad esempio processori di schede di chiamata a distanza estesa.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




