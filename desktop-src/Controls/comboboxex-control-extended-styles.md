---
title: Stili estesi del controllo ComboBoxEx (CommCtrl.h)
description: Supporta gli stili estesi elencati in questa sezione e la maggior parte degli stili di controllo casella combinata standard.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387657"
---
# <a name="comboboxex-control-extended-styles"></a>Stili estesi del controllo ComboBoxEx

Supporta gli stili estesi elencati in questa sezione e la maggior parte degli stili di controllo casella combinata standard.



| Costante                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ EX \_ CASESENSITIVE**</dt> </dl>             | **Per le ricerche BSTR** nell'elenco verrà effettuata la distinzione tra maiuscole e minuscole. Sono incluse le ricerche in seguito alla digitazione di testo nella casella di modifica e nel messaggio CB \_ FINDSTRINGEXACT.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | La casella di modifica e l'elenco a discesa non visualizzano le immagini degli elementi. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | La casella di modifica e l'elenco a discesa non visualizzano le immagini degli elementi. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | Consente di ridimensionare verticalmente il controllo ComboBoxEx rispetto al relativo controllo casella combinata contenuto. Se le dimensioni di ComboBoxEx sono inferiori a quelle della casella combinata, la casella combinata verrà ritagliata. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | Windows NT solo. Nella casella di modifica verranno utilizzati i caratteri barra (/), barra rovesciata ( \\ ) e punto (.) come delimitatori di parole. In questo modo i tasti di scelta rapida per lo spostamento del cursore parola per parola sono efficaci nei nomi di percorso e negli URL.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista e versioni successive.** Determina il troncamento degli elementi nell'elenco a discesa e nella casella di modifica (quando la casella di modifica è di sola lettura) con puntini di sospensione ("...") anziché semplicemente ritagliati dal bordo del controllo. Ciò è utile quando il controllo deve essere impostato su una larghezza fissa, ma le voci nell'elenco possono essere lunghe.<br/> |



## <a name="remarks"></a>Commenti

È possibile impostare e recuperare gli stili estesi della casella combinata usando i messaggi [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) e [**CBEM \_ GETEXTENDEDSTYLE.**](cbem-getextendedstyle.md)

> [!Note]  
> Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo stile [**SIMPLE di \_ CBS,**](combo-box-styles.md) potrebbe non essere ridisegnato correttamente. Anche **lo stile \_ SIMPLE** di CBS non funziona correttamente con lo stile esteso CBES \_ EX \_ PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





