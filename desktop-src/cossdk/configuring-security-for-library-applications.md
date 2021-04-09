---
description: Per configurare la sicurezza basata sui ruoli e l'autenticazione per le applicazioni di libreria, è necessario tenere presenti alcune considerazioni speciali.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configurazione della sicurezza per le applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102d6a0f102bfd19da0073bca14df8a8211203b1
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103968808"
---
# <a name="configuring-security-for-library-applications"></a>Configurazione della sicurezza per le applicazioni di libreria

Per configurare la sicurezza basata sui ruoli e l'autenticazione per le applicazioni di libreria, è necessario tenere presenti alcune considerazioni speciali.

## <a name="enabling-or-disabling-authentication"></a>Abilitazione o disabilitazione dell'autenticazione

Uno dei fattori da considerare è che i chiamanti dell'applicazione libreria devono essere soggetti ai controlli di sicurezza a livello di processo del processo di hosting, ovvero se abilitare o disabilitare l'autenticazione.

Se, ad esempio, l'applicazione libreria sarà ospitata da un browser, potrebbe essere necessario ricevere callback non autenticati. Per rispondere a questa esigenza, è possibile disabilitare l'autenticazione in modo che il processo di hosting non esegua controlli di sicurezza per i chiamanti dell'applicazione della libreria. Quando si disabilita l'autenticazione, l'applicazione della libreria non viene autenticata, tutte le chiamate a tale applicazione riusciranno. I chiamanti dell'applicazione libreria non sono soggetti ai controlli di sicurezza del processo di hosting. In pratica, l'applicazione della libreria viene contrassegnata come "non autenticata" e i controlli di sicurezza vengono omessi per le chiamate all'applicazione della libreria.

Per informazioni su come abilitare o disabilitare l'autenticazione, vedere Abilitazione dell' [autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Applicazione di controlli di ruolo

Un'altra decisione da prendere consiste nel fatto che l'applicazione di libreria debba utilizzare la [protezione basata sui ruoli](role-based-security-administration.md). Se si usa la sicurezza basata sui ruoli, è necessario usare la sicurezza a livello di componente per eseguire tutti i controlli di accesso. I ruoli assegnati all'applicazione libreria non vengono riflessi nel descrittore di sicurezza del processo. L'unica autorizzazione che l'applicazione della libreria è in grado di controllare è a livello di componente. Per ulteriori informazioni sulla sicurezza a livello di componente, vedere [limiti di sicurezza](security-boundaries.md).

Per informazioni su come impostare la sicurezza a livello di componente, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Scenari di configurazione

Per comprendere meglio le implicazioni di decidere se l'applicazione di libreria deve utilizzare la protezione basata sui ruoli e se l'applicazione di libreria deve essere non autenticata, considerare gli scenari seguenti:

-   **L'autenticazione è abilitata e viene utilizzata la sicurezza basata sui ruoli.** In questo scenario, i controlli di sicurezza vengono eseguiti dal processo di hosting e ad alcuni chiamanti viene negato l'accesso a livello di processo. Il controllo dei ruoli viene inoltre eseguito a livello di applicazione della libreria, in modo che per alcuni chiamanti che lo eseguono tramite il controllo di sicurezza a livello di processo venga negato l'accesso all'applicazione libreria quando viene controllata l'appartenenza al ruolo. Si tratta dello scenario usuale per un'applicazione libreria COM+ che usa la sicurezza basata sui ruoli.

    Nella figura seguente viene illustrato lo scenario in cui è abilitata l'autenticazione e viene utilizzato il controllo del ruolo.

    ![Diagramma che illustra l'autenticazione che avviene in un processo host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **L'autenticazione è abilitata e non viene usata la protezione basata sui ruoli.** In questo scenario, i controlli di sicurezza vengono eseguiti a livello di processo, ma l'appartenenza al ruolo non viene controllata a livello di applicazione della libreria. Pertanto, qualsiasi chiamante dell'applicazione della libreria che lo esegue tramite il controllo di sicurezza a livello di processo potrà accedere all'applicazione libreria perché l'appartenenza al ruolo non viene controllata. Questa situazione si verifica quando viene eseguita la migrazione di un'applicazione COM che non usa la sicurezza basata sui ruoli in un'applicazione libreria COM+.

    Nella figura seguente viene illustrato lo scenario in cui l'autenticazione è abilitata e non viene utilizzato il controllo del ruolo.

    ![Diagramma che illustra l'autenticazione a livello di processo per un'applicazione libreria all'interno del processo host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **L'autenticazione è disabilitata e viene utilizzata la sicurezza basata sui ruoli.** In questo scenario, i controlli di sicurezza vengono eseguiti a livello di processo, ma i chiamanti per l'applicazione della libreria non sono autenticati. In effetti, i chiamanti dell'applicazione libreria sono esenti dal controllo di sicurezza a livello di processo. Poiché il controllo dei ruoli è abilitato, l'appartenenza ai ruoli da solo determina gli utenti a cui viene concesso l'accesso all'applicazione della libreria. Questo scenario potrebbe essere appropriato quando il controllo di sicurezza che verrebbe eseguito dal processo di hosting è troppo restrittivo, ma è necessario disporre di una restrizione di accesso per l'applicazione libreria o per interfacce o metodi specifici. Questo scenario consente di disattivare efficacemente la sicurezza del processo e di disporre comunque di controlli di accesso a livello appropriati mediante la sicurezza basata sui ruoli.

    Nella figura seguente viene illustrato lo scenario in cui è disabilitata l'autenticazione e viene utilizzato il controllo del ruolo.

    ![Diagramma che mostra ' controlla appartenenza a ruoli ' in un'applicazione di libreria all'interno di un processo host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **L'autenticazione è disabilitata e la protezione basata sui ruoli non viene utilizzata.** In questo scenario, i controlli di sicurezza vengono ancora eseguiti a livello di processo, ma, come nello scenario precedente, i chiamanti dell'applicazione libreria passano sempre questo controllo di sicurezza. Poiché anche il controllo dei ruoli è disabilitato, l'appartenenza al ruolo non viene controllata a livello di applicazione della libreria. In pratica, chiunque può chiamare l'applicazione della libreria. Questo scenario deve essere scelto quando l'oggetto COM deve ricevere callback non autenticati, come potrebbe essere il caso di un controllo ActiveX ospitato da Internet Explorer e con uno snap-in di Microsoft Management Console. Naturalmente, questo oggetto COM deve essere considerato attendibile per un comportamento appropriato durante la ricezione di chiamate non autenticate. Ad esempio, non deve accedere ai file arbitrari per conto dei chiamanti.

    Nella figura seguente è illustrato lo scenario in cui l'autenticazione è disabilitata e il controllo del ruolo non è in uso.

    ![Diagramma che mostra le chiamate a un'applicazione di libreria che non sono autenticate all'interno del processo host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Dopo aver deciso se abilitare o disabilitare l'autenticazione per l'applicazione della libreria COM+, vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md) per una procedura dettagliata in cui viene illustrato come disabilitare o abilitare l'autenticazione mediante lo strumento di amministrazione Servizi componenti. Se l'applicazione di libreria utilizzerà la protezione basata sui ruoli, vedere [configurazione Role-Based sicurezza](configuring-role-based-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> </dl>

 

 



