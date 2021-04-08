---
title: Gestione riavvio
description: Scrivere programmi di installazione personalizzati per eliminare i riavvii del sistema necessari per completare l'aggiornamento di un file in uso. Arrestare e riavviare tutti i servizi di sistema, ma non critici, dai programmi.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gestione riavvio riavvio gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047081"
---
# <a name="restart-manager"></a>Gestione riavvio

## <a name="purpose"></a>Scopo

L'API di gestione riavvio può eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento. Il motivo principale per cui gli aggiornamenti software richiedono un riavvio del sistema durante un'installazione o un aggiornamento è che alcuni dei file che vengono aggiornati vengono attualmente utilizzati da un'applicazione o da un servizio in esecuzione. Gestione riavvio consente di arrestare e riavviare tutti i [servizi di sistema](critical-system-services.md) , tranne quelli critici. Consente di liberare i file in uso e di completare le operazioni di installazione.

## <a name="where-applicable"></a>Se applicabile

La DLL di gestione riavvio Esporta un'interfaccia C pubblica che può essere caricata da programmi di installazione standard o personalizzati. Il programma di installazione può usare Gestione riavvio per registrare i file che devono essere sostituiti durante l'installazione di un'applicazione o di un aggiornamento. Quindi, durante un aggiornamento o un'installazione successiva, il programma di installazione può usare Gestione riavvio per determinare quali file non possono essere aggiornati perché sono attualmente in uso. Gestione riavvio può arrestare e riavviare i servizi o le applicazioni non critiche che attualmente utilizzano tali file. I programmi di installazione possono indirizzare Gestione riavvio per arrestare e riavviare le applicazioni o i servizi in base al file in uso, l'ID processo (PID) o il nome breve di un servizio Windows.

Gestione riavvio è progettato per lo sviluppo di applicazioni di tipo desktop.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata agli sviluppatori di applicazioni di installazione che desiderano sfruttare le funzionalità del programma di installazione di Windows Vista o Windows Server 2008. Le applicazioni che usano la versione di [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4,0 per l'installazione e la manutenzione utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di gestione riavvio per arrestare e riavviare le applicazioni e i servizi. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di gestione riavvio per pianificare i riavvii in modo da ridurre al minimo l'alterazione del flusso di lavoro dell'utente.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API Gestione riavvio è disponibile a partire da Windows Vista e Windows Server 2008. Gestione riavvio è costituito da una singola DLL che le applicazioni possono caricare per accedere all'API di gestione riavvio.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Informazioni su Gestione riavvio](about-restart-manager.md)<br/>         | Argomenti introduttivi che descrivono Gestione riavvio.<br/>   |
| [Utilizzo di gestione riavvio](using-restart-manager.md)<br/>         | Argomenti introduttivi sull'uso dell'API Gestione riavvio.<br/> |
| [Riferimento a gestione riavvio](restart-manager-reference.md)<br/> | Argomenti di riferimento per l'API di gestione riavvio.<br/>        |



 

 

