---
description: Abilitazione dei controlli di accesso a livello di componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Abilitazione dei controlli di accesso a livello di componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3063873923d3d4c491312ca4efccd9bcd665b46bf1bdfc882b69dbe4942757f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047469"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Abilitazione dei controlli di accesso a livello di componente

Se l'applicazione include un componente che non richiede controlli di sicurezza, è possibile decidere di disabilitare i controlli dei ruoli per tale componente per migliorare le prestazioni. In caso di debug, può essere utile disabilitare la sicurezza in modo da concentrarsi su altri aspetti della funzionalità del programma.

Per impostazione predefinita, quando si installa un componente, i controlli di accesso a livello di componente sono abilitati. Tuttavia, questa operazione [](enabling-access-checks-for-an-application.md) ha effetto solo quando sono [](setting-a-security-level-for-access-checks.md) abilitati i controlli di accesso a livello di applicazione e quando il livello di sicurezza è impostato su Esegui controlli di accesso a livello di processo **e di componente.**

**Per abilitare o disabilitare i controlli di accesso a livello di componente**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il componente per il quale si desidera disabilitare (o abilitare) i controlli dei ruoli. Espandere la visualizzazione nell'albero per visualizzare i componenti nella **cartella** Componenti .

2.  Fare clic con il pulsante destro del mouse sul componente per il quale si desidera abilitare i controlli dei ruoli, quindi **scegliere Proprietà.**

3.  Nella finestra di dialogo proprietà componente fare clic sulla **scheda** Sicurezza .

4.  Selezionare **Imponi controlli di accesso a livello di componente** per applicare i controlli a livello di componente.

5.  Fare clic su **OK**.

La nuova impostazione verrà attivata al successivo avvio dell'applicazione.

> [!Note]  
> A Windows Server 2003, i controlli di accesso a livello di componente sono disabilitati per impostazione predefinita durante la creazione di un'applicazione COM+. I controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente. In precedenza, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurazione della Role-Based sicurezza](configuring-role-based-security.md)
</dt> <dt>

[Definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



