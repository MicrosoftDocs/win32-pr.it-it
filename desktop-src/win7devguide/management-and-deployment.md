---
title: Gestione e distribuzione
description: I professionisti IT o gli sviluppatori che preparano la distribuzione di Windows 7 avranno una maggiore confidenza e un ciclo di valutazione più breve grazie ai miglioramenti apportati alle funzionalità e agli strumenti di imaging.
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963230"
---
# <a name="management-and-deployment"></a>Gestione e distribuzione

I professionisti IT o gli sviluppatori che preparano la distribuzione di Windows 7 avranno una maggiore confidenza e un ciclo di valutazione più breve grazie ai miglioramenti apportati alle funzionalità e agli strumenti di imaging. Sono inclusi il supporto per la gestione di applicazioni, driver e sistemi operativi nei file di immagine offline. Inoltre, la creazione e la gestione delle immagini saranno più semplici e saranno disponibili per una gamma più ampia di organizzazioni IT. La distribuzione di Windows 7 nei computer aziendali sarà inoltre più semplice e rapida grazie ai nuovi strumenti di migrazione IT e alle tecnologie di distribuzione automatica.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell è un linguaggio di scripting gestito Microsoft .NET completo che dispone di una shell della riga di comando interattiva e di un ambiente di scripting integrato (ISE) con interfaccia grafica. Supporta la diramazione, il ciclo, le funzioni, il debug, la gestione delle eccezioni e l'internazionalizzazione. PowerShell 2,0 fa parte di Windows 7 e fornisce numerosi miglioramenti e un set di *cmdlet* in continua crescita per diagnostica Windows, Microsoft Active Directory, Microsoft Internet Information Services (IIS) e altro ancora.

La funzionalità di comunicazione remota di PowerShell 2,0 consente ora agli utenti di eseguire comandi in uno o più computer remoti da un singolo computer che esegue PowerShell. Gli sviluppatori possono inoltre ospitare PowerShell in IIS per accedere e gestire i server.

PowerShell 2,0 supporta il partizionamento e l'organizzazione di script di PowerShell usando moduli che possono essere distribuiti e distribuiti come unità indipendenti e riutilizzabili. Include anche il supporto delle transazioni nel motore di PowerShell e nelle API, il che significa che gli sviluppatori possono avviare, eseguire il commit e il rollback delle transazioni usando i *cmdlet* di transazione predefiniti. Il motore di PowerShell include inoltre il supporto per gli eventi per l'ascolto, l'invio e la gestione di eventi di sistema e di gestione. È possibile scrivere applicazioni PowerShell per sottoscrivere determinati eventi per l'elaborazione sincrona o asincrona. (Vedere [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx)).

![Screenshot di Windows PowerShell ISE](images/windows7-devguide-solidfig1-powershell.jpg)

Figura 1. Windows PowerShell è un linguaggio di scripting gestito .NET completo che dispone di una shell della riga di comando interattiva e di un'interfaccia grafica ISE

## <a name="windows-installer"></a>Windows Installer

Windows Installer è stato aggiornato in modo da aumentare l'efficienza degli sviluppatori riducendo la quantità di codice personalizzato necessario per creare un pacchetto di installazione e creare installazioni software reali per singolo utente.

La transazione di più pacchetti consente agli sviluppatori di creare una singola transazione da più pacchetti usando un "Chainer" per includere dinamicamente i pacchetti nella transazione. Se uno o più pacchetti non vengono installati come previsto, è sufficiente eseguire il rollback dell'installazione.

Il gestore dell'interfaccia utente incorporato rende più semplice l'integrazione delle interfacce utente personalizzate incorporando un gestore dell'interfaccia utente personalizzato nel pacchetto di Windows Installer.

Embedded multiple Package Chainer consente agli sviluppatori di abilitare gli eventi di installazione tra più pacchetti. Ad esempio, possono abilitare gli eventi di installazione su richiesta, ripristinare gli eventi e disinstallare gli eventi tra più pacchetti.

Le nuove funzionalità consentono inoltre la creazione di vere installazioni per utente, incluso il supporto per i file di programma per utente e la funzionalità "elevare ora", e forniscono supporto per l'inventario software offline e i controlli di applicabilità delle patch tramite la gestione e la manutenzione delle immagini di distribuzione. Vedere Novità [di Windows Installer 5,0](../msi/what-s-new-in-windows-installer-5-0.md).

 

 