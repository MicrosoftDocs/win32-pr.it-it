---
description: Windows Installer è conforme a controllo dell'account utente (UAC) in Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Uso di Windows Installer con UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a05dcd2fb33eff24fb17702af1cb306f81002d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130267"
---
# <a name="using-windows-installer-with-uac"></a>Uso di Windows Installer con UAC

Windows Installer è conforme a [*controllo dell'account utente*](u-gly.md) (UAC) in Windows Vista. Con l'autorizzazione di un amministratore, il Windows Installer può installare le applicazioni o le patch per conto di un utente che potrebbe non essere un membro del gruppo Administrators. Questa operazione viene definita installazione con [*privilegi elevati*](e-gly.md) , perché il Windows Installer apporta modifiche al sistema per conto dell'utente che in genere non è consentito se l'utente ha apportato le modifiche direttamente.

-   Quando si utilizza Windows Vista in un ambiente aziendale, le applicazioni possono essere designate come applicazioni gestite. Utilizzando la distribuzione dell'applicazione e [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page), gli amministratori possono bloccare le directory e quindi assegnare o pubblicare le applicazioni gestite in tali directory agli [*utenti standard*](s-gly.md) per l'installazione, il ripristino o la rimozione. Le applicazioni gestite vengono registrate nell'hive del registro di sistema del **\_ \_ computer locale HKEY** . Dopo che un'applicazione è stata registrata come applicazione gestita, le successive operazioni di installazione vengono sempre eseguite con privilegi elevati. Se l'utente è in esecuzione come amministratore, non è richiesto alcun messaggio di richiesta per continuare l'installazione. Se l'utente è in esecuzione come utente standard e l'applicazione è già stata assegnata o pubblicata, l'installazione dell'applicazione gestita può continuare senza richiedere conferma.
-   Quando si utilizza Windows Vista in un ambiente non aziendale, il controllo dell'account utente gestisce l'elevazione dell'installazione dell'applicazione. Windows Installer 4,0 può chiamare il [*servizio informazioni applicazioni*](a-gly.md) (AIS) per richiedere l'autorizzazione dell'amministratore per elevare un'installazione. Prima che sia possibile eseguire un'installazione di che richiede privilegi di amministratore, UAC chiede all'utente il consenso per elevare l'installazione. La richiesta di consenso viene visualizzata per impostazione predefinita, anche se l'utente è un membro del gruppo Administrators locale, perché gli amministratori vengono eseguiti come utenti standard finché un'applicazione o un componente di sistema che richiede credenziali amministrative richiede l'autorizzazione per l'esecuzione. Questa esperienza utente è denominata [*modalità Approvazione amministratore*](a-gly.md) (AAM). Se un utente standard tenta di installare l'applicazione, l'utente deve disporre di privilegi di amministratore per fornire le credenziali di amministratore per continuare l'installazione. Questa esperienza utente è detta richiesta di credenziali OTS ( [*over the Shoulder*](o-gly.md) ).
-   Poiché il controllo dell'account utente limita i privilegi durante le fasi di un'installazione, gli sviluppatori dei pacchetti di Windows Installer non devono presupporre che l'installazione possa sempre accedere a tutte le parti del sistema. Gli sviluppatori di pacchetti Windows Installer devono quindi rispettare le linee guida per i pacchetti descritte nelle [linee guida per i pacchetti](guidelines-for-packages.md) per assicurarsi che il pacchetto funzioni con UAC e Windows Vista. Un pacchetto che è stato creato e testato per conformarsi a UAC deve contenere la proprietà [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) impostata su 1.
-   Un amministratore può anche usare i metodi descritti nella sezione: [installazione di un pacchetto con privilegi elevati per un utente non](installing-a-package-with-elevated-privileges-for-a-non-admin.md) amministratore per consentire a un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.
-   I privilegi sono necessari per installare un'applicazione nel contesto gestito per utente e, di conseguenza, le reinstallazioni Windows Installer successive o le riparazioni dell'applicazione vengono eseguite anche dal programma di installazione con privilegi elevati. Ciò significa che solo le patch provenienti da origini attendibili possono essere applicate a un'applicazione nello stato gestito per utente. A partire da Windows Installer 3,0, è possibile applicare una patch a un'applicazione gestita per utente dopo la registrazione della patch con privilegi elevati. Per informazioni, vedere [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md).

> [!Note]  
> Quando non sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto può disattivare la finestra di dialogo visualizzata da UAC per richiedere l'autorizzazione dell'amministratore. Per ulteriori informazioni, vedere [creazione di pacchetti senza la finestra di dialogo controllo dell'account utente](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
