---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131514"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibilità**
</dt> <dd>

Implementazione di progettazione per rendere accessibile l'interfaccia utente del programma di installazione a tutti gli utenti. Per ulteriori informazioni sull'accessibilità, vedere l'argomento introduttivo: [accessibilità](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase di acquisizione**
</dt> <dd>

Fase di installazione durante la quale il programma di installazione determina la procedura. La fase di acquisizione inizia quando un'applicazione o un utente indica [*Windows Installer*](m-gly.md) di installare un'applicazione o una funzionalità. Il programma di installazione esegue quindi una query nel [*database*](i-gly.md) per ottenere informazioni quando genera lo [*script di esecuzione*](e-gly.md) per l'installazione. Per ulteriori informazioni sulle fasi di un'installazione di, vedere [meccanismo di installazione](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**azione**
</dt> <dd>

Molte delle funzioni eseguite da Windows Installer sono incapsulate in azioni. Ogni azione specifica l'esecuzione di una particolare funzione e il flusso procedurale totale dell'installazione viene richiesto dalla sequenza di azioni nelle [*tabelle di sequenza*](s-gly.md). Le [*azioni standard*](s-gly.md) sono incorporate in Windows Installer. Le [*azioni personalizzate*](c-gly.md) vengono scritte dall'autore del [*pacchetto*](p-gly.md)di installazione.

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modalità Approvazione amministratore**
</dt> <dd>

Lo stato di approvazione abilitato dalla protezione dell'account utente (UAC) che esegue tutti gli utenti con privilegi minimi, inclusi gli amministratori. Agli utenti viene richiesto di fornire il consenso per elevare le installazioni che richiedono privilegi di amministratore.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**pubblicità**
</dt> <dd>

Funzionalità per rendere le interfacce necessarie per il caricamento e per rendere disponibile un'applicazione senza installare l'applicazione. Quando un utente o un'applicazione attiva un'interfaccia annunciata, il programma di installazione procede quindi con l'installazione dei componenti necessari. I due tipi di annunci pubblicitari sono [*assegnazione*](/windows) e [*pubblicazione*](p-gly.md). Per altre informazioni, vedere anche [*installare su richiesta*](i-gly.md). Per ulteriori informazioni sul modo in cui il programma di installazione annuncia le applicazioni, vedere l' [annuncio](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Servizio informazioni applicazioni (AIS)**
</dt> <dd>

Un servizio di sistema di Windows Vista che facilita l'avvio di installazioni che richiedono privilegi elevati per l'esecuzione. Fornisce l'interfaccia utente di consenso utilizzata da controllo dell'account utente per richiedere all'utente l'autorizzazione di amministratore.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assegnazione**
</dt> <dd>

Rende disponibile un'applicazione e la rende visibile come se fosse stata installata a un utente, senza installarla effettivamente. L'assegnazione di aggiunge collegamenti e icone al menu **Start** , associa i file appropriati e scrive le voci del registro di sistema per l'applicazione. Quando un utente tenta di aprire un'applicazione assegnata, il programma di installazione installa l'applicazione. L'assegnazione e la [*pubblicazione*](p-gly.md) sono due metodi di [*annuncio pubblicitario*](/windows). Per ulteriori informazioni, vedere l' [annuncio](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**esecuzione asincrona**
</dt> <dd>

[*Azione personalizzata*](c-gly.md) durante la quale il programma di installazione esegue contemporaneamente thread distinti dell'azione personalizzata e dell'installazione corrente. Per altre informazioni, vedere [azioni personalizzate sincrone e asincrone](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
