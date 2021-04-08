---
description: In questa sezione viene descritta la cronologia delle versioni per la tecnologia Tablet PC.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Cronologia della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f258876f79f8e701ed59242233dcccc292b15f52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058195"
---
# <a name="tablet-pc-platform-history"></a>Cronologia della piattaforma Tablet PC

In questa sezione viene descritta la cronologia delle versioni per la tecnologia Tablet PC.

## <a name="platform-description"></a>Descrizione della piattaforma

I componenti della tecnologia Tablet PC consentono di sviluppare applicazioni progettate per l'hardware di Tablet PC.

Questi componenti possono essere utilizzati per compilare applicazioni eseguite in Windows XP Tablet PC Edition 2005, Windows Vista, Windows 7, Windows Server 2008 R2 e in alcuni altri sistemi operativi precedenti.

Il Windows Presentation Foundation supporta anche lo sviluppo di applicazioni Tablet PC.

## <a name="version-history"></a>Cronologia versioni

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Piattaforma Tablet in Windows 7 e Windows Server 2008 R2

Windows 7 introduce un supporto linguistico aggiuntivo, il controllo di input matematico e i dizionari personalizzati. Anche le funzionalità di [Windows Touch](../wintouch/windows-touch-portal.md) sono state aggiunte ai sistemi operativi Windows.

Windows Server 2008 R2 introduce il supporto per lingue aggiuntive, dizionari personalizzati e riconoscimento lato server.

Le funzionalità seguenti migliorano la funzionalità di Tablet e consentono agli sviluppatori di distribuire nuove applicazioni che supportano scenari pratici per gli utenti finali.

-   Il controllo di input matematico consente di inserire formule e funzioni matematiche da testo scritto a mano in Windows 7.
-   Per migliorare il riconoscimento del testo, Windows 7 e Windows Server 2008 R2 supportano dizionari personalizzati, in modo che gli amministratori possano abilitare direttamente il supporto per gli elenchi di parole.
-   Windows Touch supporta l'input da più origini touch tramite nuovi messaggi della finestra, oltre a un'API di riconoscimento movimento che supporta la panoramica, lo zoom e la rotazione.
-   Windows Server 2008 R2 supporta il riconoscimento lato server dell'input del form e supporta anche dizionari personalizzati per il riconoscimento lato server. Con l'aggiunta di queste funzionalità, gli sviluppatori e gli amministratori possono creare e personalizzare potenti applicazioni che supportano il riconoscimento della grafia dal lato server.

### <a name="tablet-platform-in-windows-vista"></a>Piattaforma Tablet in Windows Vista

I file binari della tecnologia Tablet PC sono stati aggiornati in Windows Vista. La tecnologia Tablet PC aggiornata include nuove API di analisi dell'input penna e una versione COM delle API di input dello stilo. Le applicazioni scritte con le versioni precedenti della tecnologia Tablet PC vengono eseguite in Windows Vista senza modifiche.

I componenti della tecnologia Tablet PC sono disponibili solo come parte del Windows SDK a partire dal rilascio di Windows Vista. Per ulteriori informazioni, vedere Novità relative [allo sviluppo di Tablet PC](what-s-new-in-tablet-pc-development.md).

### <a name="version-17"></a>Versione 1,7

Tablet PC Development Kit 1,7 ha esteso le funzionalità di sviluppo oltre a quelle disponibili nella versione 1,5, aggiungendo le API di input dello stilo e il supporto per l'input penna sul Web.

In passato, la funzionalità della versione 1,5 era in un file binario separato, ma in Tablet PC Development Kit 1,7 tutte le funzionalità venivano inserite in un unico file binario.

### <a name="version-15"></a>Versione 1.5

La versione 1,5 del kit di sviluppo ha sostituito la versione 1,1. Fornisce le API del pannello input penna e l'oggetto divisore.

> [!Note]  
> Se si installa Tablet PC Development Kit versione 1,5, dopo l'installazione è necessario ristabilire i riferimenti all'assembly Microsoft Ink nelle applicazioni scritte con le versioni precedenti di Tablet PC SDK prima della compilazione e dell'esecuzione di.

 

### <a name="version-11"></a>Versione 1.1

La versione 1,1 del kit di sviluppo ha sostituito la versione 1,0. La versione 1,1 è costituita esclusivamente da aggiornamenti alla documentazione; i file binari della piattaforma non sono stati modificati tra la versione 1,1 del kit di sviluppo e la versione fornita di Windows XP Tablet PC Edition. Pertanto, le applicazioni sviluppate con la versione 1,1 Development Kit non devono ridistribuire i componenti per utilizzare le funzionalità della piattaforma quando vengono installati nei tablet PC.

> [!Note]  
> Le applicazioni distribuite a sistemi operativi non Tablet PC possono utilizzare un sottoinsieme di funzionalità della piattaforma Tablet PC. Queste applicazioni devono includere il modulo merge ridistribuito fornito nella versione 1,1 Development Kit con la relativa configurazione.

 

### <a name="version-10"></a>Versione 1,0

La versione 1,0 del kit di sviluppo è stata sostituita dalla versione 1,1.

 

 
