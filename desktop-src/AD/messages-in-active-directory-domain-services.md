---
title: Messaggi in Active Directory Domain Services
description: I messaggi in Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4,0 con Service Pack 6a (SP6a) e versioni successive con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- ANNUNCIO Active Directory messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297723"
---
# <a name="messages-in-active-directory-domain-services"></a>Messaggi in Active Directory Domain Services

I messaggi in Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4,0 con Service Pack 6a (SP6a) e versioni successive con DSClient. Sono anche funzionali nelle workstation Windows 98/95 con IE 4.01 e versioni successive e DSClient. Se, tuttavia, le pagine delle proprietà MultiSelect vengono avviate dalla shell, il messaggio di [**\_ \_ \_ errore WM ADSPROP Notify**](wm-adsprop-notify-error.md) e le funzioni helper corrispondenti, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) , non sono funzionali e non verranno visualizzate. Se le pagine delle proprietà MultiSelect vengono avviate all'interno di uno strumento di amministrazione, ad esempio utenti e computer di Active Directory, tutti i messaggi sono funzionali e disponibili per essere visualizzati nelle pagine delle proprietà MultiSelect.

Active Directory Domain Services utilizzare i messaggi seguenti:

-   [**richiesta di notifica di WM \_ ADSPROP \_ \_**](wm-adsprop-notify-apply.md)
-   [**\_ \_ modifica notifica ADSPROP \_ WM**](wm-adsprop-notify-change.md)
-   [**\_errore di \_ notifica \_ ADSPROP di WM**](wm-adsprop-notify-error.md)
-   [**\_ \_ uscita notifica ADSPROP \_ WM**](wm-adsprop-notify-exit.md)
-   [**\_ \_ primo piano della notifica ADSPROP WM \_**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ Notify \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ Notify \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**STATO di notifica di WM \_ ADSPROP \_ \_**](wm-adsprop-notify-setfocus.md)
-   [**\_ \_ creazione foglio ADSPROP \_ WM**](wm-adsprop-sheet-create.md)
-   [**\_notifica di \_ chiusura del foglio DSA \_ WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ creazione \_ notifica foglio DSA WM**](wm-dsa-sheet-create-notify.md)

 

 




