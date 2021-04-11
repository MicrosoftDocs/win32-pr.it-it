---
description: Dopo aver abilitato i controlli di accesso, per l'applicazione COM+ è necessario selezionare il livello in cui si desidera che vengano eseguiti i controlli di accesso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Impostazione di un livello di sicurezza per i controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127395"
---
# <a name="setting-a-security-level-for-access-checks"></a>Impostazione di un livello di sicurezza per i controlli di accesso

Dopo aver abilitato i [controlli di accesso](enabling-access-checks-for-an-application.md), per l'applicazione com+ è necessario selezionare il livello in cui si desidera che vengano eseguiti i controlli di accesso.

**Per selezionare un livello di sicurezza**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si desidera abilitare i controlli di accesso, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  In **livello di sicurezza**, selezionare una delle opzioni seguenti:

    -   **Esegui controlli di accesso solo a livello di processo**: questa impostazione indica che gli utenti nei ruoli assegnati all'applicazione verranno aggiunti al descrittore di sicurezza del processo. Ciò presenta gli effetti e le implicazioni seguenti:

        Il controllo dei ruoli con granularità fine è disattivato a livello di componente, metodo e interfaccia. I controlli di sicurezza vengono eseguiti solo a livello di applicazione.

        La proprietà di sicurezza non è inclusa nel contesto per gli oggetti in esecuzione all'interno dell'applicazione. Questo può influire potenzialmente sulla modalità di attivazione degli oggetti. Vedere [proprietà del contesto di sicurezza](security-context-property.md).

        Il contesto della chiamata di sicurezza non verrà reso disponibile. La sicurezza a livello di codice che si basa sulle informazioni sul contesto delle chiamate di sicurezza non funzionerà. Vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

    -   **Eseguire i controlli di accesso a livello di processo e componente**: questa impostazione indica che verranno eseguiti i controlli dei descrittori di sicurezza a livello di processo e i controlli di sicurezza completi basati sui ruoli. Ciò presenta gli effetti e le implicazioni seguenti:

        Per abilitare il controllo dei ruoli per determinati componenti, è necessario [abilitare i controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md).

        La proprietà di sicurezza è inclusa nel contesto per qualsiasi oggetto in esecuzione all'interno dell'applicazione. Questo può influire potenzialmente sulla modalità di attivazione degli oggetti. Vedere [proprietà del contesto di sicurezza](security-context-property.md).

        Il contesto della chiamata di sicurezza è disponibile. La sicurezza basata sui ruoli a livello di codice è abilitata. Vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

        > [!Note]  
        > Per le applicazioni della libreria COM+, è necessario scegliere di controllare i livelli a livello di processo e di componente per eseguire il controllo di accesso significativo. Le applicazioni di libreria si basano sul processo host per la sicurezza a livello di processo. È possibile determinare il modo in cui l'applicazione della libreria interagisce con l'autenticazione eseguita dal processo host [impostando l'autenticazione](enabling-authentication-for-a-library-application.md). Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).

         

4.  Fare clic su **OK**.

Al successivo avvio dell'applicazione, la sicurezza verrà controllata automaticamente al livello specificato. Solo agli utenti assegnati ai ruoli assegnati all'applicazione verrà concesso l'accesso all'applicazione.

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

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



