---
description: L'esecuzione di questo passaggio consente di controllare l'accesso ai processi o la sicurezza completa basata sui ruoli, a seconda del livello di sicurezza selezionato e se si Abilita il controllo degli accessi per i singoli componenti.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Abilitazione dei controlli di accesso per un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304617"
---
# <a name="enabling-access-checks-for-an-application"></a>Abilitazione dei controlli di accesso per un'applicazione

L'esecuzione di questo passaggio consente di controllare l'accesso ai processi o la sicurezza completa basata sui ruoli, a seconda del livello di sicurezza selezionato e se si Abilita il controllo degli accessi per i singoli componenti.

**Per abilitare i controlli di accesso per un'applicazione**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si desidera abilitare i controlli di accesso, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  Selezionare la casella **di controllo applica verifiche di accesso per l'applicazione** .

4.  Fare clic su **OK**.

> [!Note]  
> A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita quando si crea un'applicazione COM+. I controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente. In precedenza, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente.

 

Dopo aver abilitato i controlli di accesso, è necessario selezionare il livello di sicurezza appropriato. Vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md). Inoltre, è necessario assicurarsi di definire i ruoli e aggiungerli all'applicazione. Se i controlli di accesso sono abilitati ma non sono stati aggiunti ruoli, tutte le chiamate all'applicazione avranno esito negativo. Vedere [definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md).

> [!Note]  
> Quando si esegue il debug dell'applicazione, potrebbe essere utile disabilitare la sicurezza in modo da potersi concentrare su altri aspetti del comportamento e della progettazione del programma.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



