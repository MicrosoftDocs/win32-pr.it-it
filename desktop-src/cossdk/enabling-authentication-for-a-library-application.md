---
description: Abilitazione dell'autenticazione per un'applicazione libreria
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Abilitazione dell'autenticazione per un'applicazione libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb3d5799ee8fac1d8eb266e6513c4d2a759adb10b78b2117424b08f8c5d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736420"
---
# <a name="enabling-authentication-for-a-library-application"></a>Abilitazione dell'autenticazione per un'applicazione libreria

Poiché le applicazioni di libreria COM+ sono ospitate da altri processi, i relativi requisiti di sicurezza possono essere diversi da quelli delle applicazioni server. Se l'applicazione libreria sarà ospitata da un browser, potrebbe essere necessario ricevere callback non autenticati.

Per risolvere questa esigenza, è possibile disabilitare l'autenticazione in modo che il processo di hosting non esezioni controlli di sicurezza per i chiamanti dell'applicazione libreria. Quando si disabilita l'autenticazione, le chiamate all'applicazione libreria vengono effettivamente non autenticate. Tutte le chiamate a questa funzione avranno esito positivo. Per altre informazioni, vedere [Sicurezza delle applicazioni della libreria.](library-application-security.md)

**Per abilitare (o disabilitare) l'autenticazione per un'applicazione libreria**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta abilitando o disabilitando l'autenticazione, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo delle proprietà dell'applicazione fare clic **sulla scheda** Sicurezza .

3.  In **Autenticazione** selezionare la casella **di controllo Abilita** autenticazione per abilitare l'autenticazione. Se si deseleziona la casella di controllo, l'autenticazione verrà disabilitata.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



