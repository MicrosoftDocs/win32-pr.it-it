---
description: La configurazione della sicurezza e dell'autenticazione basata sui ruoli per le applicazioni di libreria è un'importante considerazione.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configurazione della sicurezza per le applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0d8b3993a00512c20409f1f029b7402d5f9ace97984cbe9757453b5672125f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548908"
---
# <a name="configuring-security-for-library-applications"></a>Configurazione della sicurezza per le applicazioni di libreria

La configurazione della sicurezza e dell'autenticazione basata sui ruoli per le applicazioni di libreria è un'importante considerazione.

## <a name="enabling-or-disabling-authentication"></a>Abilitazione o disabilitazione dell'autenticazione

Uno dei fattori da considerare è se i chiamanti dell'applicazione libreria devono essere soggetti ai controlli di sicurezza a livello di processo del processo di hosting, ovvero se abilitare o disabilitare l'autenticazione.

Ad esempio, se l'applicazione libreria sarà ospitata da un browser, potrebbe essere necessario ricevere callback non autenticati. Per risolvere questa esigenza, è possibile disabilitare l'autenticazione in modo che il processo di hosting non esezioni controlli di sicurezza per i chiamanti dell'applicazione di libreria. Quando si disabilita l'autenticazione, l'applicazione di libreria diventa effettivamente non autenticata. Tutte le chiamate a avranno esito positivo. I chiamanti dell'applicazione libreria non sono soggetti ai controlli di sicurezza del processo di hosting. In pratica, l'applicazione di libreria è contrassegnata come "non autenticata" e i controlli di sicurezza vengono omessi per le chiamate all'applicazione libreria.

Per informazioni su come abilitare o disabilitare l'autenticazione, vedere [Abilitazione dell'autenticazione per un'applicazione libreria](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Applicazione dei controlli dei ruoli

Un'altra decisione da prendere è se l'applicazione di libreria deve usare [la sicurezza basata sui ruoli.](role-based-security-administration.md) Se si usa la sicurezza basata sui ruoli, è necessario usare la sicurezza a livello di componente per eseguire eventuali controlli di accesso. I ruoli assegnati all'applicazione di libreria non vengono riflessi nel descrittore di sicurezza del processo. L'unica autorizzazione che l'applicazione di libreria può controllare è a livello di componente. Per altre informazioni sulla sicurezza a livello di componente, vedere [Limiti di sicurezza](security-boundaries.md).

Per informazioni su come impostare la sicurezza a livello di componente, vedere [Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Scenari di configurazione

Per comprendere meglio le implicazioni di decidere se l'applicazione di libreria deve usare la sicurezza basata sui ruoli e se l'applicazione di libreria deve essere non autenticata, considerare gli scenari seguenti:

-   **L'autenticazione è abilitata e viene usata la sicurezza basata sui ruoli.** In questo scenario, i controlli di sicurezza vengono eseguiti dal processo di hosting e ad alcuni chiamanti viene negato l'accesso a livello di processo. Inoltre, il controllo dei ruoli viene eseguito a livello di applicazione della libreria in modo che ad alcuni chiamanti che eccedono il controllo di sicurezza a livello di processo non sia consentito l'accesso all'applicazione di libreria quando viene verificata l'appartenenza al ruolo. Questo è lo scenario consueto per un'applicazione libreria COM+ che usa la sicurezza basata sui ruoli.

    La figura seguente illustra lo scenario in cui è abilitata l'autenticazione e viene usato il controllo dei ruoli.

    ![Diagramma che illustra l'autenticazione in corso all'interno di un processo host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **L'autenticazione è abilitata e la sicurezza basata sui ruoli non viene usata.** In questo scenario, i controlli di sicurezza vengono eseguiti a livello di processo, ma l'appartenenza al ruolo non viene verificata a livello di applicazione della libreria. Pertanto, qualsiasi chiamante dell'applicazione di libreria che esegue il controllo di sicurezza a livello di processo avrà accesso all'applicazione libreria perché l'appartenenza al ruolo non viene controllata. Questa situazione si verifica quando viene eseguita la migrazione di un'applicazione COM che non usa la sicurezza basata sui ruoli a un'applicazione libreria COM+.

    La figura seguente illustra lo scenario in cui l'autenticazione è abilitata e il controllo dei ruoli non viene usato.

    ![Diagramma che illustra l'autenticazione a livello di processo per un'applicazione libreria all'interno del processo host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **L'autenticazione è disabilitata e viene usata la sicurezza basata sui ruoli.** In questo scenario, i controlli di sicurezza vengono eseguiti a livello di processo, ma i chiamanti dell'applicazione di libreria non sono autenticati. In effetti, i chiamanti dell'applicazione libreria sono esentati dal controllo di sicurezza a livello di processo. Poiché il controllo dei ruoli è abilitato, l'appartenenza al ruolo determina da solo chi può accedere all'applicazione di libreria. Questo scenario potrebbe essere appropriato quando il controllo di sicurezza che verrebbe eseguito dal processo di hosting è troppo restrittivo, ma è necessario applicare alcune restrizioni di accesso all'applicazione libreria o a interfacce o metodi specifici. Questo scenario consente di disattivare in modo efficace la sicurezza dei processi e di avere comunque un controllo di accesso di livello appropriato usando la sicurezza basata sui ruoli.

    Lo scenario in cui l'autenticazione è disabilitata e viene usato il controllo dei ruoli è illustrato nella figura seguente.

    ![Diagramma che illustra la verifica dell'appartenenza al ruolo in un'applicazione libreria all'interno di un processo host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **L'autenticazione è disabilitata e la sicurezza basata sui ruoli non viene usata.** In questo scenario, i controlli di sicurezza vengono comunque eseguiti a livello di processo, ma, come nello scenario precedente, i chiamanti dell'applicazione di libreria superano sempre questo controllo di sicurezza. Poiché anche il controllo dei ruoli è disabilitato, l'appartenenza al ruolo non viene verificata a livello di applicazione della libreria. In sostanza, chiunque può chiamare l'applicazione di libreria. Questo scenario deve essere scelto quando l'oggetto COM deve ricevere callback non autenticati, come nel caso di un controllo ActiveX ospitato da Internet Explorer e con uno snap-in Microsoft Management Console. Naturalmente, questo oggetto COM deve essere considerato attendibile per comportarsi in modo appropriato quando si ricevono chiamate non autenticate. Ad esempio, non deve accedere a file arbitrari per conto dei chiamanti.

    Lo scenario in cui l'autenticazione è disabilitata e il controllo dei ruoli non viene usato è illustrato nella figura seguente.

    ![Diagramma che mostra le chiamate a un'applicazione di libreria non autenticate all'interno del processo host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Dopo aver deciso se abilitare o disabilitare l'autenticazione [](enabling-authentication-for-a-library-application.md) per l'applicazione libreria COM+, vedere abilitazione dell'autenticazione per un'applicazione libreria per una procedura dettagliata che spiega come disabilitare o abilitare l'autenticazione usando lo strumento amministrativo Servizi componenti. Se l'applicazione di libreria userà la sicurezza basata sui ruoli, vedere [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> </dl>

 

 



