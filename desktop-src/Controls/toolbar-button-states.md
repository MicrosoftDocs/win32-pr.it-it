---
title: Stati del pulsante della barra degli strumenti (CommCtrl. h)
description: Questa sezione elenca gli Stati che possono essere presenti in un pulsante della barra degli strumenti.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327591"
---
# <a name="toolbar-button-states"></a>Stati del pulsante della barra degli strumenti

Questa sezione elenca gli Stati che possono essere presenti in un pulsante della barra degli strumenti.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ selezionato**</dt> </dl>                   | Il pulsante ha lo stile di [**\_ controllo TBSTYLE**](toolbar-control-and-button-styles.md) e viene fatto clic su di esso.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**\_ellissi TBSTATE**</dt> </dl>                | [Versione 4,70](common-control-versions.md). Il testo del pulsante è troncato e vengono visualizzati i puntini di sospensione.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ abilitato**</dt> </dl>                   | Il pulsante accetta l'input dell'utente. Un pulsante che non dispone di questo stato è disattivato.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ nascosto**</dt> </dl>                      | Il pulsante non è visibile e non è in grado di ricevere l'input dell'utente.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ INdeterminato**</dt> </dl> | Il pulsante è disattivato.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ contrassegnato come**</dt> </dl>                      | [Versione 4,71](common-control-versions.md). Il pulsante è contrassegnato. L'interpretazione di un elemento contrassegnato dipende dall'applicazione. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ premuto**</dt> </dl>                   | Si fa clic sul pulsante.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**TBSTATE a \_ capo**</dt> </dl>                            | Il pulsante è seguito da un'interruzioni di riga. Il pulsante deve avere anche lo \_ stato abilitato per TBSTATE.<br/>                                              |



## <a name="remarks"></a>Commenti

Una barra degli strumenti può avere una combinazione di Stati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





