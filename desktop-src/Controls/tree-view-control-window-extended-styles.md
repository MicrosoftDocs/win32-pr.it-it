---
title: Tree-View degli stili estesi del controllo (CommCtrl.h)
description: Questa sezione elenca gli stili estesi usati durante la creazione di controlli visualizzazione albero. Il valore degli stili estesi è una combinazione bit per bit di questi stili.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed135e5c1cfd335333251c183b408a59d2768ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477387"
---
# <a name="tree-view-control-extended-styles"></a>Tree-View degli stili estesi del controllo

Questa sezione elenca gli stili estesi usati durante la creazione di controlli visualizzazione albero. Il valore degli stili estesi è una combinazione bit per bit di questi stili.




| Costante | Descrizione | 
|----------|-------------|
| <span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl><dt><strong>TVS_EX_AUTOHSCROLL</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Rimuovere la barra di scorrimento orizzontale e lo scorrimento automatico a seconda della posizione del mouse.<br /> | 
| <span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl><dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Includere lo stato della casella di controllo in grigio se il controllo ha lo <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> predefinito.<br /> | 
| <span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl><dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Specifica la modalità di cancellazione o riempimento dello sfondo.<br /> | 
| <span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl><dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Recupera le informazioni sulla griglia del calendario.<br /> | 
| <span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl><dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Includere lo stato della casella di controllo di esclusione se il controllo ha lo <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> predefinito.<br /> | 
| <span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl><dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Dissolvenza dei pulsanti expando in entrata o in uscita quando il mouse si sposta o passa al passaggio del mouse sul controllo.<br /> | 
| <span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl><dt><strong>TVS_EX_MULTISELECT</strong></dt></dl> | Non supportata. Non usare.<br /> | 
| <span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl><dt><strong>TVS_EX_NOINDENTSTATE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Non fare rientro nella visualizzazione albero per i pulsanti expando.<br /> | 
| <span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl><dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. <strong>Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.</strong> Non comprimere l'elemento della visualizzazione albero selezionato in precedenza a meno che non abbia lo stesso elemento padre della nuova selezione. Questo stile deve essere usato con lo <a href="tree-view-control-window-styles.md"><strong>stile TVS_SINGLEEXPAND</strong></a> predefinito. <br /><blockquote>[!Note]<br />Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll. Inoltre, questo stile non è definito in commctrl.h. Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code></blockquote><br /> | 
| <span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl><dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Includere lo stato della casella di controllo parziale se il controllo ha lo <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> controllo.<br /> | 
| <span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl><dt><strong>TVS_EX_RICHTOOLTIP</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Consente descrizioni comando rtf nella visualizzazione albero (personalizzata disegnata con icona e testo).<br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





