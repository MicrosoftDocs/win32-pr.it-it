---
description: Questa sezione descrive la cronologia delle versioni per La tecnologia Tablet PC.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Cronologia della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78cbcecd8ee02f56a4d89b2ca9d14217da277525dd3548adec7282d6744d1d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843051"
---
# <a name="tablet-pc-platform-history"></a>Cronologia della piattaforma Tablet PC

Questa sezione descrive la cronologia delle versioni per La tecnologia Tablet PC.

## <a name="platform-description"></a>Descrizione della piattaforma

I componenti della tecnologia Tablet PC consentono di sviluppare applicazioni progettate per l'hardware tablet PC.

Questi componenti possono essere usati per compilare applicazioni eseguite in Windows XP Tablet PC Edition 2005, Windows Vista, Windows 7, Windows Server 2008 R2 e in alcuni altri sistemi operativi precedenti.

Il Windows Presentation Foundation supporta anche lo sviluppo di applicazioni Tablet PC.

## <a name="version-history"></a>Cronologia versioni

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Piattaforma tablet in Windows 7 e Windows Server 2008 R2

Windows 7 introduce il supporto linguistico aggiuntivo, il controllo di input matematico e i dizionari personalizzati. [Windows funzionalità Touch](../wintouch/windows-touch-portal.md) sono state aggiunte anche ai Windows operativi.

Windows Server 2008 R2 introduce il supporto per lingue aggiuntive, dizionari personalizzati e riconoscimento lato server.

Le funzionalità seguenti migliorano la funzionalità tablet e consentono agli sviluppatori di distribuire nuove applicazioni che supportano scenari pratici per gli utenti finali.

-   Il controllo di input matematico consente l'input di formule matematiche e funzioni dal testo scritto a mano Windows 7.
-   Per migliorare il riconoscimento del testo, Windows 7 e Windows Server 2008 R2 supportano dizionari personalizzati in modo che gli amministratori possano abilitare direttamente il supporto per gli elenchi di parole.
-   Windows Il tocco supporta l'input da più origini di tocco tramite nuovi messaggi della finestra, oltre a un'API di riconoscimento dei movimenti che supporta la panoramica, lo zoom e la rotazione.
-   Windows Server 2008 R2 supporta il riconoscimento lato server dell'input del modulo e supporta anche dizionari personalizzati per il riconoscimento lato server. Con l'aggiunta di queste funzionalità, sviluppatori e amministratori possono creare e personalizzare applicazioni potenti che supportano il riconoscimento della grafia dal lato server.

### <a name="tablet-platform-in-windows-vista"></a>Piattaforma tablet in Windows Vista

I file binari della tecnologia Tablet PC sono stati aggiornati in Windows Vista. La tecnologia Tablet PC aggiornata include nuove API di analisi dell'input penna e una versione COM delle API input penna. Le applicazioni scritte in versioni precedenti della tecnologia Tablet PC vengono eseguite Windows Vista senza modifiche.

I componenti della tecnologia Tablet PC sono disponibili solo come parte di Windows SDK a partire dal rilascio di Windows Vista. Per altre informazioni, vedere [Novità dello sviluppo di Tablet PC.](what-s-new-in-tablet-pc-development.md)

### <a name="version-17"></a>Versione 1.7

Tablet PC Development Kit 1.7 ha esteso le funzionalità di sviluppo oltre a quella disponibile nella versione 1.5, aggiungendo le API Input stilo e il supporto per l'input penna sul Web.

In passato, la funzionalità della versione 1.5 era in un file binario separato, ma in Tablet PC Development Kit 1.7 tutte le funzionalità erano inserite in un unico file binario.

### <a name="version-15"></a>Versione 1.5

La versione 1.5 di Development Kit ha sostituito la versione 1.1. Sono disponibili le API del pannello di input penna e l'oggetto Divisore.

> [!Note]  
> Se si installa Tablet PC Development Kit versione 1.5, dopo l'installazione è necessario ristabilire i riferimenti all'assembly Microsoft Ink nelle applicazioni scritte in versioni precedenti di Tablet PC SDK prima di compilare ed eseguire.

 

### <a name="version-11"></a>Versione 1.1

La versione 1.1 di Development Kit ha sostituito la versione 1.0. La versione 1.1 era costituita esclusivamente da aggiornamenti alla documentazione. i file binari della piattaforma non sono stati modificati tra la versione 1.1 del Kit di sviluppo e la versione fornita di Windows XP Tablet PC Edition. Pertanto, le applicazioni sviluppate con la versione 1.1 Development Kit non devono ridistribuire alcun componente per usare le funzionalità della piattaforma quando vengono installate nei Tablet PC.

> [!Note]  
> Le applicazioni distribuite a sistemi operativi non Tablet PC possono usare un subset di funzionalità della piattaforma Tablet PC. Queste applicazioni devono includere il modulo unione ridistribuito fornito nella versione 1.1 Development Kit con la relativa configurazione.

 

### <a name="version-10"></a>Versione 1.0

La versione 1.0 del Kit di sviluppo è stata sostituita dalla versione 1.1.

 

 
