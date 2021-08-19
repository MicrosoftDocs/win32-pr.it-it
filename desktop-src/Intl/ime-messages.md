---
description: Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Messaggi IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa34228f695a18187654707668067ac34562098b48aae185a8d66d777b6f507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949262"
---
# <a name="ime-messages"></a>Messaggi IME

Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME. Ad esempio, il sistema operativo invia il [**messaggio WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) all'applicazione quando viene attivata una finestra. Le applicazioni IME non consapevoli passano questi messaggi alla funzione [DefWindowProc,](/windows/desktop/api/winuser/nf-winuser-defwindowproca) che li invia alla finestra IME predefinita corrispondente. Le applicazioni in grado di riconoscere IME elaborano questi messaggi o li inoltrano alle proprie finestre IME.

L'applicazione può indirizzare una finestra IME per eseguire un comando, ad esempio modificare la posizione di una finestra di composizione, usando il [**messaggio WM \_ IME \_ CONTROL.**](wm-ime-control.md) L'IME notifica all'applicazione le modifiche alla stringa di composizione usando il messaggio [**WM \_ IME \_ COMPOSITION**](wm-ime-composition.md) e le modifiche generali allo stato delle finestre IME inviando il messaggio [**WM \_ IME \_ NOTIFY.**](wm-ime-notify.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
