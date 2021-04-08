---
title: Avvio e arresto di Microsoft Locator
description: Quando necessario, le librerie di runtime RPC avviano automaticamente Microsoft Locator. È possibile arrestare e avviare manualmente il localizzatore se, ad esempio, è necessario cancellare il database durante il debug di un'applicazione distribuita.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043999"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Avvio e arresto di Microsoft Locator

Quando necessario, le librerie di runtime RPC avviano automaticamente Microsoft Locator. È possibile arrestare e avviare manualmente il localizzatore se, ad esempio, è necessario cancellare il database durante il debug di un'applicazione distribuita.

**Per arrestare e avviare Microsoft Locator**

1.  Nel pannello di controllo fare clic sull'icona servizi.

    Verrà visualizzata la finestra di dialogo **Servizi** .

2.  Nella finestra di dialogo **servizio** selezionare **Microsoft Locator** , quindi fare clic su **Avvia** o **Arresta**.

È anche possibile avviare e arrestare Microsoft Locator dalla riga di comando digitando:

**NET \[ Start/Stop \] RpcLocator**

Solo un amministratore può avviare Microsoft Locator dopo che è stato arrestato. Se arrestata, verrà riavviata in base alle esigenze delle librerie di runtime RPC.

 

 




