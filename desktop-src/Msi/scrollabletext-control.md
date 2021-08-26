---
description: Questo controllo visualizza una lunga stringa di testo che non può essere adattata interamente alla pagina. Un uso comune per questo controllo è la visualizzazione del contratto di licenza.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Controllo ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f4d5ac48f6b89b779960126e62c204d1d09e1f9a7bc832b0e3477635df35ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041301"
---
# <a name="scrollabletext-control"></a>Controllo ScrollableText

Questo controllo visualizza una lunga stringa di testo che non può essere adattata interamente alla pagina. Un uso comune per questo controllo è la visualizzazione del contratto di licenza.

Si noti che la stringa di testo usata con questo controllo non può contenere una proprietà incorporata. Per visualizzare il testo con proprietà incorporate, usare invece [il controllo Text](text-control.md).

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md) o [BBControl](bbcontrol-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Testo visualizzato dal controllo . Immettere la stringa di testo RTF nella colonna Testo della [tabella Control](control-table.md).                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Per rendere il controllo visibile o nascosto durante la creazione, includere questo bit nella parola di bit della colonna Attributi nella tabella [Control](control-table.md) o [BBControl](bbcontrol-table.md).<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella colonna Attributi delle tabelle [Control](control-table.md) o [BBControl](bbcontrol-table.md) per abilitare il controllo durante la creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Consente di visualizzare lo stile di visualizzazione predefinito. Visualizzare il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Il testo nel controllo viene visualizzato in ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | La barra di scorrimento si trova sul lato destro del controllo . La barra di scorrimento si trova sul lato sinistro del controllo .<br/>                                                                                                                                                                                                                                              |
| [Bidi](bidi-control-attribute.md)                 | 0x000000E0                       | Impostare questo valore per una combinazione degli [attributi RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md) [e LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe RICHEDIT usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Include gli stili **ES \_ MULTILINE,** **WS \_ VSCROLL,** **ES \_ READONLY,** **WS \_ TABSTOP,** **ES \_ AUTOVSCROLL,** **WS \_ CHILD,** **WS \_ GROUP** ed **ES \_ NOOLEDRAGDROP.**

 

 
