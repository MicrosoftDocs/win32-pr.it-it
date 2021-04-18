---
title: Costanti SELFLAG (oleacc. h)
description: In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione di un oggetto accessibile o lo stato attivo.
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
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327702"
---
# <a name="selflag-constants"></a>Costanti SELFLAG

In questo argomento vengono descritti i valori costanti utilizzati per specificare la modalità di selezione di un oggetto accessibile o lo stato attivo. Le costanti sono definite in oleacc. h e vengono usate con il metodo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .

Non sono consentite le combinazioni seguenti:

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Nota ai client:** Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli Edit e Rich Edit perché il testo viene esposto come stringa nella [proprietà Value](value-property.md)dell'oggetto.

Per informazioni su come eseguire operazioni di selezione complesse, vedere [selezione di oggetti figlio](selecting-child-objects.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Non esegue alcuna azione. Microsoft Active Accessibility non modifica la selezione o lo stato attivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </dl></td>
<td style="text-align: left;">Imposta lo stato attivo sull'oggetto e lo rende l'ancoraggio della selezione. Usato da solo, questo flag non modifica la selezione. L'effetto è simile allo spostare lo stato attivo manualmente premendo un tasto di direzione tenendo premuto il tasto CTRL in Esplora risorse o in qualsiasi casella di riepilogo a selezione multipla. <br/> Con gli oggetti con il <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS viene combinato con i valori seguenti:<br/>
<ul>
<li>SELFLAG_TAKESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li>
</ul>
Se si chiama <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> con il flag SELFLAG_TAKEFOCUS su un oggetto con <strong>HWND</strong>, il flag diviene effettivo solo se l'elemento padre dell'oggetto ha già lo stato attivo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </dl></td>
<td style="text-align: left;">Seleziona l'oggetto e rimuove la selezione da tutti gli altri oggetti nel contenitore. <br/> A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione. SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinazione è equivalente a un solo clic su un elemento in Esplora risorse.<br/> Questo flag non deve essere combinato con i flag seguenti:<br/>
<ul>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </dl></td>
<td style="text-align: left;">Modifica la selezione in modo che tutti gli oggetti tra l'ancoraggio di selezione e questo oggetto prendano lo stato di selezione dell'oggetto di ancoraggio. Se tale oggetto non è selezionato, gli oggetti verranno rimossi dalla selezione. Se l'oggetto di ancoraggio è selezionato, la selezione viene estesa in modo da includere questo oggetto e tutti gli oggetti in. Impostare lo stato di selezione combinando questo flag con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION. <br/> A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione. SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale all'aggiunta manuale di un elemento a una selezione tenendo premuto il tasto MAIUSC e facendo clic su un oggetto non selezionato in Esplora risorse.<br/> Questo flag non è combinato con SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </dl></td>
<td style="text-align: left;">Aggiunge l'oggetto alla selezione corrente. il risultato possibile è una selezione non contigua. <br/> A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione. SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinazione equivale all'aggiunta manuale di un elemento a una selezione tenendo premuto il tasto CTRL e facendo clic su un oggetto non selezionato in Esplora risorse.<br/> Questo flag non è combinato con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </dl></td>
<td style="text-align: left;">Rimuove l'oggetto dalla selezione corrente. il risultato possibile è una selezione non contigua. <br/> A meno che non sia combinato con SELFLAG_TAKEFOCUS, questo flag non modifica lo stato attivo o l'ancoraggio della selezione. SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinazione equivale a rimuovere un elemento da una selezione manualmente, tenendo premuto il tasto CTRL mentre si fa clic su un oggetto selezionato in Esplora risorse.<br/> Questo flag non è combinato con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Selezione di oggetti figlio](selecting-child-objects.md)
</dt> </dl>

 

 





