---
description: Dopo aver abilitato i controlli di accesso, per l'applicazione COM+, è necessario selezionare il livello a cui si desidera eseguire i controlli di accesso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Impostazione di un livello di sicurezza per i controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e912f671a27d35b51939376fa14af3b693c368e3375680913693d364ddf638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120371"
---
# <a name="setting-a-security-level-for-access-checks"></a>Impostazione di un livello di sicurezza per i controlli di accesso

Dopo aver abilitato i controlli [di accesso](enabling-access-checks-for-an-application.md)per l'applicazione COM+, è necessario selezionare il livello a cui si desidera eseguire i controlli di accesso.

**Per selezionare un livello di sicurezza**

1.  Nell'albero della console dello strumento amministrativo Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si desidera abilitare i controlli di accesso e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo delle proprietà dell'applicazione fare clic **sulla scheda** Sicurezza .

3.  In **Livello di** sicurezza selezionare una delle opzioni seguenti:

    -   **Esegui controlli di accesso solo a** livello di processo: questa impostazione indica che gli utenti nei ruoli assegnati all'applicazione verranno aggiunti al descrittore di sicurezza del processo. Ciò ha gli effetti e le implicazioni seguenti:

        Il controllo granulare dei ruoli è disattivato a livello di componente, metodo e interfaccia. I controlli di sicurezza vengono eseguiti solo a livello di applicazione.

        La proprietà di sicurezza non è inclusa nel contesto per gli oggetti in esecuzione all'interno dell'applicazione. Ciò può influire potenzialmente sulla modalità di attivazione degli oggetti. Vedere [Proprietà del contesto di sicurezza](security-context-property.md).

        Il contesto di chiamata di sicurezza non verrà reso disponibile. La sicurezza a livello di codice basata sulle informazioni sul contesto delle chiamate di sicurezza non funzionerà. Vedere [Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

    -   **Esegui controlli di accesso a livello di** processo e di componente: questa impostazione indica che verranno eseguiti i controlli dei descrittori di sicurezza a livello di processo e i controlli di sicurezza completi basati sui ruoli. Ciò ha gli effetti e le implicazioni seguenti:

        Per abilitare il controllo dei ruoli per componenti specifici, è necessario [abilitare i controlli di accesso a livello di componente.](enabling-access-checks-at-the-component-level.md)

        La proprietà di sicurezza è inclusa nel contesto per tutti gli oggetti in esecuzione all'interno dell'applicazione. Ciò può influire potenzialmente sulla modalità di attivazione degli oggetti. Vedere [Proprietà del contesto di sicurezza](security-context-property.md).

        Il contesto di chiamata di sicurezza è disponibile. La sicurezza basata sui ruoli a livello di codice è abilitata. Vedere [Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

        > [!Note]  
        > Per le applicazioni di libreria COM+, è necessario scegliere di controllare sia a livello di processo che a livello di componente per il funzionamento di qualsiasi controllo di accesso significativo. Le applicazioni di libreria si basano sul processo host per la sicurezza a livello di processo. È possibile determinare il modo in cui l'applicazione di libreria interagisce con l'autenticazione eseguita dal processo host impostando [l'autenticazione](enabling-authentication-for-a-library-application.md). Per altre informazioni, vedere [Sicurezza delle applicazioni della libreria.](library-application-security.md)

         

4.  Fare clic su **OK**.

Al successivo avvio dell'applicazione, la sicurezza verrà verificata automaticamente al livello specificato. Solo gli utenti assegnati ai ruoli assegnati all'applicazione avranno accesso all'applicazione.

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

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



