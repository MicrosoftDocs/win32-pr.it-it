---
title: Installazione di applicazioni su sistemi a 64 bit
description: Il Windows Installer a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- Programmazione Windows a 64 bit per l'installazione dell'applicazione
- installazione della programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118015"
---
# <a name="application-installation-on-64-bit-systems"></a>Installazione di applicazioni su sistemi a 64 bit

Il [Windows Installer a 64 bit](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit. Per le applicazioni meno recenti che usano uno stub a 16 bit per avviare un motore di installazione a 32 bit, Windows a 64 bit riconosce specifici programmi del programma di installazione a 16 bit e sostituisce una versione a 32 bit portata.

le applicazioni DOS, Windows o OS/2 a 16 bit utilizzano spesso uno stub a 16 bit per verificare il tipo di computer, quindi avviano un motore di installazione a 32 bit per eseguire effettivamente l'installazione. Per consentire l'installazione di applicazioni che utilizzano questa tecnica, Windows a 64 bit sostituisce le versioni a 32 bit per i seguenti programmi del programma di installazione a 16 bit:

* Installazione Microsoft per Windows 1,2  
* Installazione Microsoft per Windows 2,6  
* Installazione Microsoft per Windows 3,0  
* Installazione Microsoft per Windows 3,01  
* InstallShield 5. x  

L'elenco di sostituzioni viene archiviato nel registro di sistema con la chiave seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Questo meccanismo è disponibile solo per la compatibilità con le applicazioni a 32 bit che usano i programmi Microsoft Installer a 16 bit elencati in questo argomento. L'aggiunta di programmi di installazione di terze parti non è supportata.

 

> [!Note]  
> Questo meccanismo non è incluso in Windows 10 su ARM.

 

 

 