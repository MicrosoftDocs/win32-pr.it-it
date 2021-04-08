---
description: Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Messaggi IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049558"
---
# <a name="ime-messages"></a>Messaggi IME

Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME. Ad esempio, il sistema operativo invia il messaggio di [**\_ \_ contesto di WM IME**](wm-ime-setcontext.md) all'applicazione quando una finestra viene attivata. Le applicazioni non compatibili con IME passano questi messaggi alla funzione [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , che li invia alla finestra IME predefinita corrispondente. Le applicazioni in grado di riconoscere gli IME elaborano questi messaggi o le inviano alla propria finestra IME.

L'applicazione può indirizzare una finestra IME per eseguire un comando, ad esempio modificare la posizione di una finestra di composizione, usando il messaggio [**di \_ \_ controllo di WM IME**](wm-ime-control.md) . L'IME notifica all'applicazione le modifiche apportate alla stringa di composizione utilizzando il messaggio di [**\_ \_ composizione IME WM**](wm-ime-composition.md) e le modifiche generali apportate allo stato delle finestre IME inviando il messaggio di [**\_ \_ notifica di WM IME**](wm-ime-notify.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
