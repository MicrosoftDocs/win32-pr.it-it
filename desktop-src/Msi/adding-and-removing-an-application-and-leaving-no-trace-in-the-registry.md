---
description: Se è necessario registrare un'applicazione, creare il pacchetto di installazione come descritto nella sezione aggiunta e rimozione delle chiavi del registro di sistema per l'installazione o la rimozione di componenti.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967299"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema

Se è necessario registrare un'applicazione, creare il pacchetto di installazione come descritto nella sezione [aggiunta e rimozione delle chiavi del registro di sistema per l'installazione o la rimozione di componenti](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). La registrazione viene utilizzata dal programma di installazione per l'annuncio e dalla funzionalità Installazione applicazioni nel pannello di controllo. Se un'applicazione non è registrata, non può essere annunciata e non è inclusa nella funzionalità Installazione applicazioni del pannello di controllo.

È possibile omettere la registrazione di un'applicazione rimuovendo l'azione [RegisterProduct](registerproduct-action.md), azione [RegisterUser](registeruser-action.md), [azione PublishProduct](publishproduct-action.md)e [PublishFeatures azione](publishfeatures-action.md) dalla tabella [InstallExecuteSequence](installexecutesequence-table.md) e [AdvtExecuteSequence tabella](advtexecutesequence-table.md). Tutte queste azioni devono essere rimosse o una traccia dell'applicazione può rimanere nel registro di sistema. La rimozione di tutte le azioni impedisce che l'applicazione venga elencata nella funzionalità Installazione applicazioni nel pannello di controllo e impedisce l'annuncio dell'applicazione. La rimozione di tutte queste azioni impedisce inoltre la registrazione dell'applicazione con i dati di configurazione Windows Installer. Ciò significa che non è possibile rimuovere, ripristinare o reinstallare l'applicazione usando le opzioni della [riga di comando](command-line-options.md)Windows Installer o l'Windows Installer Application Programming Interface (API).

Per nascondere un'applicazione dalla funzionalità Installazione applicazioni nel pannello di controllo e comunque essere in grado di utilizzare il Windows Installer per gestire un'applicazione, lasciare le azioni di registrazione nelle tabelle di sequenza e impostare la [**Proprietà ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) nella tabella delle [Proprietà](property-table.md) su 1 (uno). L'applicazione non viene visualizzata nella funzionalità Installazione applicazioni, ma è possibile usare la Windows Installer per installare su richiesta, disinstallare, ripristinare e reinstallare l'applicazione.

 

 



