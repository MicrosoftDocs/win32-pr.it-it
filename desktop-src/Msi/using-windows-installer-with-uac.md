---
description: Windows Il programma di installazione è conforme a Controllo dell'account utente in Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Uso del Windows con Controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458d6265938f44a694366e8145d60aa5d031d47e715932502bd1b82e7012b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942281"
---
# <a name="using-windows-installer-with-uac"></a>Uso del Windows con Controllo dell'account utente

Windows Il programma di installazione è conforme [*a Controllo dell'account*](u-gly.md) utente in Windows Vista. Con l'autorizzazione di un amministratore, il programma di installazione di Windows può installare applicazioni o patch per conto di un utente che potrebbe non essere membro del gruppo Administrators. Questa operazione viene definita [](e-gly.md) installazione con privilegi elevati perché il programma di installazione di Windows apporta modifiche al sistema per conto dell'utente che normalmente non sarebbero consentite se l'utente apportasse le modifiche direttamente.

-   Quando si Windows Vista in un ambiente aziendale, le applicazioni possono essere designate come applicazioni gestite. Usando la distribuzione di applicazioni [e Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page), gli amministratori possono bloccare le directory e quindi assegnare o pubblicare le applicazioni gestite in tali directory agli utenti [*standard*](s-gly.md) per l'installazione, il ripristino o la rimozione. Le applicazioni gestite vengono registrate nell'hive del Registro di sistema **HKEY \_ LOCAL \_ MACHINE.** Dopo che un'applicazione è stata registrata come applicazione gestita, le operazioni di installazione successive vengono sempre eseguite con privilegi elevati. Se l'utente è in esecuzione come amministratore, non è necessaria alcuna richiesta per continuare l'installazione. Se l'utente è in esecuzione come utente standard e l'applicazione è già stata assegnata o pubblicata, l'installazione dell'applicazione gestita può continuare senza chiedere conferma.
-   Quando si usa Windows Vista in un ambiente non aziendale, Controllo dell'account utente gestisce l'elevazione dei privilegi dell'installazione dell'applicazione. Windows Il programma di installazione 4.0 può chiamare [*application information service*](a-gly.md) (AIS) per richiedere l'autorizzazione dell'amministratore per elevare i privilegi di installazione. Prima di eseguire un'installazione identificata come che richiede privilegi di amministratore, controllo dell'account utente richiede all'utente il consenso per elevare l'installazione. La richiesta di consenso viene visualizzata per impostazione predefinita, anche se l'utente è membro del gruppo Administrators locale, perché gli amministratori vengono eseguiti come utenti standard fino a quando un'applicazione o un componente di sistema che richiede credenziali amministrative richiede l'autorizzazione per l'esecuzione. Questa esperienza utente è denominata Modalità approvazione amministratore (AAM, [*Admin Approval Mode).*](a-gly.md) Se un utente standard tenta di installare l'applicazione, deve ottenere una persona con privilegi di amministratore per fornire le credenziali di amministratore per continuare l'installazione. Questa esperienza utente è detta richiesta [*di credenziali OTS (Over the Shoulder).*](o-gly.md)
-   Poiché Controllo dell'account utente limita i privilegi durante le fasi di un'installazione, gli sviluppatori di pacchetti del programma di installazione di Windows non devono presupporre che l'installazione abbia sempre accesso a tutte le parti del sistema. Windows Gli sviluppatori di pacchetti del programma di installazione devono pertanto rispettare le linee guida per i pacchetti descritte in [Linee](guidelines-for-packages.md) guida per i pacchetti per garantire il funzionamento del pacchetto con Controllo dell'account utente Windows Vista. Un pacchetto creato e testato per la conformità al controllo dell'account utente deve contenere la proprietà [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) impostata su 1.
-   Un amministratore può anche usare i metodi descritti nella sezione Installazione di un pacchetto con privilegi elevati per un utente non amministratore per consentire [a](installing-a-package-with-elevated-privileges-for-a-non-admin.md) un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.
-   I privilegi sono necessari per installare un'applicazione nel contesto gestito dall'utente e pertanto le successive reinstallazioni o ripristino del programma di installazione di Windows vengono eseguite anche dal programma di installazione con privilegi elevati. Ciò significa che solo le patch provenienti da origini attendibili possono essere applicate a un'applicazione nello stato gestito per utente. A partire da Windows Installer 3.0, è possibile applicare una patch a un'applicazione gestita per utente dopo che la patch è stata registrata con privilegi elevati. Per informazioni, vedere [Applicazione di Per-User applicazioni gestite.](patching-per-user-managed-applications.md)

> [!Note]  
> Quando non sono necessari privilegi elevati per installare un pacchetto del programma di installazione di Windows, l'autore del pacchetto può eliminare la finestra di dialogo visualizzata da Controllo dell'account utente per richiedere agli utenti l'autorizzazione dell'amministratore. Per altre informazioni, vedere Creazione di pacchetti senza la finestra di dialogo [Controllo dell'account utente](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
