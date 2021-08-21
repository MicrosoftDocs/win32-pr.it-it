---
title: Messaggi in Active Directory Domain Services
description: I messaggi Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4.0 con Service Pack 6a (SP6a) e versioni successive con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory Messages AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025919"
---
# <a name="messages-in-active-directory-domain-services"></a>Messaggi in Active Directory Domain Services

I messaggi Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4.0 con Service Pack 6a (SP6a) e versioni successive con DSClient. Sono anche funzionali nelle Windows 98/95 con IE4.01 e versioni successive e DSClient. Tuttavia, se le pagine delle proprietà a selezione multipla vengono avviate dalla shell, il messaggio [**WM \_ ADSPROP \_ NOTIFY \_ ERROR**](wm-adsprop-notify-error.md) e le funzioni helper corrispondenti, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) non sono funzionali e non verranno visualizzati. Se le pagine delle proprietà a selezione multipla vengono avviate all'interno di uno strumento di amministrazione, ad esempio Utenti e computer di Active Directory, tutti i messaggi sono funzionali e possono essere visualizzati all'interno delle pagine delle proprietà a selezione multipla.

Active Directory Domain Services usare i messaggi seguenti:

-   [**APPLICAZIONE \_ DI WM ADSPROP \_ \_ NOTIFY**](wm-adsprop-notify-apply.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ CHANGE**](wm-adsprop-notify-change.md)
-   [**ERRORE \_ DI NOTIFICA DI ADSPROP \_ \_ WM**](wm-adsprop-notify-error.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ EXIT**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ FOREGROUND**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
-   [**NOTIFICA \_ DI CHIUSURA DEL FOGLIO WM DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md)
-   [**NOTIFICA \_ DI CREAZIONE FOGLIO WM DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md)

 

 




