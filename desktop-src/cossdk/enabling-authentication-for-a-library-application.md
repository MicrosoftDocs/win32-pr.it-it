---
description: Abilitazione dell'autenticazione per un'applicazione di libreria
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Abilitazione dell'autenticazione per un'applicazione di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305012"
---
# <a name="enabling-authentication-for-a-library-application"></a>Abilitazione dell'autenticazione per un'applicazione di libreria

Poiché le applicazioni di libreria COM+ sono ospitate da altri processi, i requisiti di sicurezza possono essere diversi da quelli delle applicazioni server. Se l'applicazione di libreria sarà ospitata da un browser, potrebbe essere necessario ricevere callback non autenticati.

Per rispondere a questa esigenza, è possibile disabilitare l'autenticazione in modo che il processo di hosting non esegua controlli di sicurezza per i chiamanti dell'applicazione della libreria. Quando si disabilita l'autenticazione, le chiamate all'applicazione di libreria vengono eseguite in modo non autenticato. tutte le chiamate ad essa verranno eseguite correttamente. Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).

**Per abilitare o disabilitare l'autenticazione per un'applicazione di libreria**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta abilitando o disabilitando l'autenticazione, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  In **autenticazione** selezionare la casella di controllo **Abilita autenticazione** per abilitare l'autenticazione. Se si deseleziona la casella di controllo, l'autenticazione viene disabilitata.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



