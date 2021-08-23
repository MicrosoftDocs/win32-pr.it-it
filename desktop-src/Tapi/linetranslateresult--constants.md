---
description: Le costanti del flag di bit LINETRANSLATERESULT \_ descrivono vari risultati di una conversione degli indirizzi.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: LINETRANSLATERESULT_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba28c04bc52d3857d76bffefed5fe07803954e72f4a5e7e05ffa22d4ee6c646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518781"
---
# <a name="linetranslateresult_-constants"></a>Costanti LINETRANSLATERESULT \_

Le costanti del flag di bit **LINETRANSLATERESULT \_** descrivono vari risultati di una conversione degli indirizzi.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ CANONICAL**
</dt> <dd> <dl> <dt>



Indica che la stringa di input è in formato canonico valido.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene "$".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIAGNOE**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene una "W".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene un "?".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo restituito contiene "@".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ INTERNATIONAL**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata internazionale (il codice paese o area geografica specificato nell'indirizzo di destinazione è diverso dal codice paese o area geografica specificato per **CurrentLocation).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



Indica che la chiamata locale viene chiamata come lunga distanza perché il paese o l'area geografica ha un numero di pedaggio e il prefisso viene visualizzato nell'elenco **TollPrefixList** di **CurrentLocation.**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ LOCAL**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata locale (il codice paese o area geografica e il codice area specificati nell'indirizzo di destinazione sono gli stessi specificati per **CurrentLocation).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene considerata come una chiamata a lunga distanza (il codice paese o area geografica specificato nell'indirizzo di destinazione è lo stesso, ma il codice area è diverso da quello specificato per **CurrentLocation).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Indica che il paese o l'area geografica supporta la chiamata a pedaggio, ma il prefisso non viene visualizzato in **TollPrefixList,** quindi la chiamata viene chiamata come chiamata locale. Si noti che se sia INTOLLIST che NOTINTOLLIST sono disattivati, il paese o l'area geografica corrente non supporta i prefissi di pedaggio e gli elementi dell'interfaccia utente correlati ai prefissi dei pedaggi non devono essere presentati all'utente; Se uno di questi bit è attivato, il paese o l'area geografica supporta gli elenchi di pedaggi e gli elementi dell'interfaccia utente correlati devono essere abilitati.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOTRANSLATION**
</dt> <dd> <dl> <dt>



Indica che la conversione degli indirizzi non è disponibile. Questo elemento viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Indica che l'indirizzo dialable restituito contiene ":". Questo elemento viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.

> [!Note]  
> Il carattere ":" (due punti) verrà aggiunto all'elenco di caratteri che possono essere incorporati in una stringa componibile e passati negli indirizzi di destinazione. Se si tenta di passarlo da un'applicazione a un dispositivo line che supporta una versione dell'API precedente alla 2.0, è molto probabile che LINEERR INVALADDRESS o eventualmente il carattere venga ignorato \_ completamente. Il significato di questo carattere è "Pause until a voice prompt is detected, then continue dialing"; è destinato all'uso durante la composizione automatica in sistemi che forniscono richieste vocali, ad esempio processori di schede da chiamata a lunga distanza.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




