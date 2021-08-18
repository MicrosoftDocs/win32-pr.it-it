---
title: Gestione riavvio
description: Scrivere programmi di installazione personalizzati per eliminare i riavvii del sistema necessari per completare l'aggiornamento di un file in uso. Arrestare e riavviare tutti i servizi di sistema, ad esempio critici, dai programmi.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gestione riavvio Gestione riavvio Mgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67910428fb781a5ddf8e2c719d30f2f0488e11d6b07daad1770788e8ad5f5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010099"
---
# <a name="restart-manager"></a>Gestione riavvio

## <a name="purpose"></a>Scopo

L'API di Gestione riavvio può eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento. Il motivo principale per cui gli aggiornamenti software richiedono un riavvio del sistema durante un'installazione o un aggiornamento è che alcuni dei file in fase di aggiornamento vengono attualmente usati da un'applicazione o un servizio in esecuzione. Gestione riavvio consente di arrestare e [riavviare](critical-system-services.md) tutti i servizi di sistema critici, ad esempio i servizi critici. In questo modo vengono liberati i file in uso e le operazioni di installazione possono essere completate.

## <a name="where-applicable"></a>Se applicabile

La DLL di Gestione riavvio esporta un'interfaccia C pubblica che può essere caricata da programmi di installazione standard o personalizzati. Il programma di installazione può usare Gestione riavvio per registrare i file che devono essere sostituiti durante l'installazione di un'applicazione o di un aggiornamento. Quindi, durante un aggiornamento o un'installazione successiva, il programma di installazione può usare Gestione riavvio per determinare quali file non possono essere aggiornati perché sono attualmente in uso. Gestione riavvio può arrestare e riavviare le applicazioni o i servizi non critici che attualmente usano tali file. I programmi di installazione possono indirizzare Gestione riavvio per arrestare e riavviare applicazioni o servizi in base al file in uso, all'ID processo (PID) o al nome breve di un servizio Windows.

Gestione riavvio è destinato allo sviluppo di applicazioni in stile desktop.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata agli sviluppatori di applicazioni di installazione che vogliono sfruttare le funzionalità del programma di installazione di Windows Vista o Windows Server 2008. Le applicazioni che usano Windows [Installer](/windows/desktop/Msi/windows-installer-portal) versione 4.0 per l'installazione e la manutenzione usano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di Gestione riavvio per arrestare e riavviare applicazioni e servizi. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di Gestione riavvio per pianificare i riavvii in modo da ridurre al minimo l'interruzione del flusso di lavoro dell'utente.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API di Gestione riavvio è disponibile a partire Windows Vista e Windows Server 2008. Gestione riavvio è costituito da una singola DLL che le applicazioni possono caricare per accedere all'API di Gestione riavvio.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Informazioni su Gestione riavvio](about-restart-manager.md)<br/>         | Argomenti di panoramica che descrivono Gestione riavvio.<br/>   |
| [Uso di Gestione riavvio](using-restart-manager.md)<br/>         | Argomenti generali sull'uso dell'API di Gestione riavvio.<br/> |
| [Informazioni di riferimento su Gestione riavvio](restart-manager-reference.md)<br/> | Argomenti di riferimento per l'API di Gestione riavvio.<br/>        |



 

 

