---
title: Stili estesi del controllo ComboBoxEx (CommCtrl. h)
description: Supportare gli stili estesi elencati in questa sezione, nonché la maggior parte degli stili standard del controllo casella combinata.
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
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327682"
---
# <a name="comboboxex-control-extended-styles"></a>Stili estesi del controllo ComboBoxEx

Supportare gli stili estesi elencati in questa sezione, nonché la maggior parte degli stili standard del controllo casella combinata.



| Costante                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ ex \_ CASESENSITIVE**</dt> </dl>             | Per le ricerche **BSTR** nell'elenco verrà fatta distinzione tra maiuscole e minuscole. Sono incluse le ricerche in seguito alla digitazione del testo nella casella di modifica e nel \_ messaggio FINDEXACTSTRING CB.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGE**</dt> </dl>                   | Nella casella di modifica e nell'elenco a discesa non vengono visualizzate le immagini dell'elemento. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt> </dl> | Nella casella di modifica e nell'elenco a discesa non vengono visualizzate le immagini dell'elemento. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ ex \_ NOSIZELIMIT**</dt> </dl>                   | Consente di ridimensionare verticalmente le dimensioni del controllo ComboBoxEx rispetto al controllo casella combinata contenuto. Se le dimensioni del ComboBoxEx sono inferiori a quelle della casella combinata, la casella combinata verrà ritagliata. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt> </dl> | Solo Windows NT. Nella casella di modifica vengono utilizzati i caratteri barra (/), barra rovesciata ( \) e punto (.) come delimitatori di parola. In questo modo, le scelte rapide da tastiera per lo spostamento di cursore Word per parola sono valide nei nomi di percorso e negli URL.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista e versioni successive.** Fa in modo che gli elementi nell'elenco a discesa e nella casella di modifica (quando la casella di modifica è di sola lettura) vengano troncati con i puntini di sospensione ("...") anziché semplicemente ritagliati per il bordo del controllo. Questa operazione è utile quando è necessario impostare il controllo su una larghezza fissa, ma le voci dell'elenco potrebbero essere lunghe.<br/> |



## <a name="remarks"></a>Commenti

È possibile impostare e recuperare gli stili estesi ComboBox usando i messaggi [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) e [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .

> [!Note]  
> Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo [**stile \_ semplice CBS**](combo-box-styles.md) , è possibile che non venga ridisegnato correttamente. Lo **stile \_ semplice CBS** non funziona anche correttamente con lo \_ \_ stile esteso CBES ex PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





