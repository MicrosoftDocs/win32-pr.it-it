---
title: Costanti SELFLAG (Oleacc.h)
description: In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione o di attivazione di un oggetto accessibile.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b4d0384b66919a55d55593d2e16c9a187d84ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478583"
---
# <a name="selflag-constants"></a>Costanti SELFLAG

In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione o di attivazione di un oggetto accessibile. Le costanti sono definite in oleacc.h e vengono usate con il [**metodo IAccessible::accSelect.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Non sono consentite le combinazioni seguenti:

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Nota per i client:** Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli di modifica e rich edit perché il testo viene esposto come stringa nella proprietà [Value dell'oggetto](value-property.md).

Per informazioni su come eseguire operazioni di selezione complesse, vedere [Selezione di oggetti figlio.](selecting-child-objects.md)




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl><dt><strong>SELFLAG_NONE</strong></dt><dt>0</dt></dl> | Non esegue alcuna azione. Microsoft Active Accessibility modifica la selezione o lo stato attivo.<br /> | 
| <span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl><dt><strong>SELFLAG_TAKEFOCUS</strong></dt><dt>0x1</dt></dl> | Imposta lo stato attivo sull'oggetto e lo rende l'ancoraggio di selezione. Usato da solo, questo flag non modifica la selezione. L'effetto è simile allo spostamento manuale dello stato attivo premendo un tasto di direzione tenendo premuto CTRL in Windows Explorer o in qualsiasi casella di riepilogo a selezione multipla. <br /> Con gli oggetti con <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS viene combinato con i valori seguenti:<br /><ul><li>SELFLAG_TAKESELECTION</li><li>SELFLAG_EXTENDSELECTION</li><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li><li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li></ul>Se si chiama <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> con il flag SELFLAG_TAKEFOCUS su un oggetto con <strong>HWND,</strong>il flag avrà effetto solo se l'elemento padre dell'oggetto ha già lo stato attivo.<br /> | 
| <span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl><dt><strong>SELFLAG_TAKESELECTION</strong></dt><dt>0x2</dt></dl> | Seleziona l'oggetto e rimuove la selezione da tutti gli altri oggetti nel contenitore. <br /> A meno che non venga combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio di selezione. Oggetto SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS è equivalente al singolo clic su un elemento in Windows Explorer.<br /> Questo flag non deve essere combinato con i flag seguenti:<br /><ul><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_EXTENDSELECTION</li></ul> | 
| <span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt><dt>0x4</dt></dl> | Modifica la selezione in modo che tutti gli oggetti tra l'ancoraggio di selezione e questo oggetto prendano lo stato di selezione dell'oggetto di ancoraggio. Se tale oggetto non è selezionato, gli oggetti verranno rimossi dalla selezione. Se l'oggetto ancoraggio è selezionato, la selezione viene estesa in modo da includere questo oggetto e tutti gli oggetti in mezzo. Impostare lo stato di selezione combinando questo flag con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION. <br /> A meno che non venga combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio di selezione. Oggetto SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale ad aggiungere manualmente un elemento a una selezione tenendo premuto MAIUSC e facendo clic su un oggetto non selezionato in Windows Explorer.<br /> Questo flag non è combinato con SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl><dt><strong>SELFLAG_ADDSELECTION</strong></dt><dt>0x8</dt></dl> | Aggiunge l'oggetto alla selezione corrente. il risultato possibile è una selezione non contigua. <br /> A meno che non venga combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio di selezione. Oggetto SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale ad aggiungere manualmente un elemento a una selezione tenendo premuto CTRL e facendo clic su un oggetto non selezionato in Windows Explorer.<br /> Questo flag non è combinato con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl><dt><strong>SELFLAG_REMOVESELECTION</strong></dt><dt>0x10</dt></dl> | Rimuove l'oggetto dalla selezione corrente. il risultato possibile è una selezione non contigua. <br /> A meno che non venga combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio di selezione. Oggetto SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS è equivalente alla rimozione manuale di un elemento da una selezione, tenendo premuto CTRL mentre si fa clic su un oggetto selezionato in Windows Explorer.<br /> Questo flag non è combinato con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.<br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Selezione di oggetti figlio](selecting-child-objects.md)
</dt> </dl>

 

 





