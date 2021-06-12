---
description: Informazioni sui Windows Installer che iniziano con la lettera A, ad esempio la fase di accessibilità e acquisizione.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011124"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Accessibilità**
</dt> <dd>

Implementazione della progettazione per rendere accessibile l'interfaccia utente del programma di installazione a tutti gli utenti. Per altre informazioni sull'accessibilità, vedere l'argomento di panoramica: [Accessibilità.](accessibility.md)

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase di acquisizione**
</dt> <dd>

Fase di installazione durante la quale il programma di installazione determina la procedura. La fase di acquisizione inizia quando un'applicazione o un utente [*Windows Installer*](m-gly.md) di installare un'applicazione o una funzionalità. Il programma di installazione esegue quindi una [*query sul database*](i-gly.md) per ottenere informazioni durante la generazione dello script di [*esecuzione*](e-gly.md) per l'installazione. Per altre informazioni sulle fasi di un'installazione, vedere [Meccanismo di installazione.](installation-mechanism.md)

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Azione**
</dt> <dd>

Molte delle funzioni eseguite da Windows Installer sono incapsulate in azioni. Ogni azione specifica l'esecuzione di una determinata funzione e il flusso procedurale totale dell'installazione è determinato dalla sequenza di azioni nelle [*tabelle sequenza*](s-gly.md). [*Le azioni*](s-gly.md) standard sono integrate in Windows Installer. [*Le azioni*](c-gly.md) personalizzate vengono scritte dall'autore del pacchetto di [*installazione*](p-gly.md).

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modalità approvazione amministratore**
</dt> <dd>

Stato di approvazione abilitato da Protezione account utente che esegue tutti gli utenti con privilegi minimi, inclusi gli amministratori. Gli utenti devono fornire il consenso per elevare i privilegi di installazione che richiedono privilegi di amministratore.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Pubblicità**
</dt> <dd>

Possibilità di rendere disponibili le interfacce necessarie per il caricamento e per rendere disponibile un'applicazione senza installare l'applicazione. Quando un utente o un'applicazione attiva un'interfaccia annunciata, il programma di installazione procede quindi all'installazione dei componenti necessari. I due tipi di annunci pubblicitari [*assegnano e*](/windows) [*pubblicano*](p-gly.md). Per altre informazioni, vedere [*anche install-on-demand.*](i-gly.md) Per altre informazioni sul modo in cui il programma di installazione annuncia le applicazioni, vedere [Advertisement](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**
</dt> <dd>

Servizio di sistema di Windows Vista che facilita l'avvio di installazioni che richiedono privilegi elevati per l'esecuzione. Fornisce l'interfaccia utente di consenso utilizzata dal controllo dell'account utente per richiedere a un utente l'autorizzazione di amministratore.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Assegnazione**
</dt> <dd>

Rende disponibile un'applicazione e la rende come se fosse stata installata per un utente, senza installarla effettivamente. L'assegnazione aggiunge collegamenti e icone al menu **Start,** associa i file appropriati e scrive le voci del Registro di sistema per l'applicazione. Quando un utente tenta di aprire un'applicazione assegnata, il programma di installazione installa l'applicazione. L'assegnazione e [*la pubblicazione*](p-gly.md) sono due metodi per [*pubblicizzare*](/windows). Per altre informazioni, vedere [Advertisement](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**esecuzione asincrona**
</dt> <dd>

[*Azione personalizzata durante*](c-gly.md) la quale il programma di installazione esegue thread separati dell'azione personalizzata e dell'installazione corrente contemporaneamente. Per altre informazioni, vedere [Azioni personalizzate sincrone e asincrone.](synchronous-and-asynchronous-custom-actions.md)

</dd> </dl>

 

 
