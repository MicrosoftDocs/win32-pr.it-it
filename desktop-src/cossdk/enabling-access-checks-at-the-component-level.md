---
description: Abilitazione dei controlli di accesso a livello di componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Abilitazione dei controlli di accesso a livello di componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304620"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Abilitazione dei controlli di accesso a livello di componente

Se l'applicazione include un componente che non necessita di controlli di sicurezza, è possibile decidere di disabilitare i controlli dei ruoli per il componente per migliorare le prestazioni. O durante il debug, potrebbe essere utile disabilitare la sicurezza in modo da potersi concentrare su altri aspetti della funzionalità del programma.

Per impostazione predefinita, quando si installa un componente sono abilitati i controlli di accesso a livello di componente. Questa operazione ha tuttavia effetto solo quando sono abilitati i [controlli di accesso a livello di applicazione](enabling-access-checks-for-an-application.md) e quando il livello di [sicurezza](setting-a-security-level-for-access-checks.md) è impostato in modo da eseguire i **controlli di accesso a livello di processo e di componente**.

**Per abilitare o disabilitare i controlli di accesso a livello di componente**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il componente per il quale si desidera disabilitare o abilitare i controlli dei ruoli. Espandere la visualizzazione nell'albero per visualizzare i componenti nella cartella **Components** .

2.  Fare clic con il pulsante destro del mouse sul componente per il quale si desidera abilitare i controlli dei ruoli, quindi scegliere **Proprietà**.

3.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **sicurezza** .

4.  Selezionare **Applica controlli di accesso a livello di componente** per applicare i controlli a livello di componente.

5.  Fare clic su **OK**.

La nuova impostazione diverrà effettiva al successivo avvio dell'applicazione.

> [!Note]  
> A partire da Windows Server 2003, i controlli di accesso a livello di componente sono disabilitati per impostazione predefinita durante la creazione di un'applicazione COM+. I controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente. In precedenza, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



