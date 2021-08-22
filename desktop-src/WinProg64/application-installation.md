---
title: Installazione di applicazioni in sistemi a 64 bit
description: Il programma di installazione Windows a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- installazione di applicazioni a 64 bit Windows programmazione
- installazione a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643601"
---
# <a name="application-installation-on-64-bit-systems"></a>Installazione di applicazioni in sistemi a 64 bit

Il programma di installazione Windows [a 64 bit](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit. Per le applicazioni meno recenti che usano uno stub a 16 bit per avviare un motore di installazione a 32 bit, Windows a 64 bit riconosce specifici programmi di installazione a 16 bit e sostituisce una versione a 32 bit con porta.

Le applicazioni DOS, Windows o OS/2 a 16 bit usano spesso uno stub a 16 bit per controllare il tipo di computer, quindi avviare un motore di installazione a 32 bit per eseguire effettivamente l'installazione. Per abilitare l'installazione di applicazioni che usano questa tecnica, Windows a 64 bit sostituisce le versioni a 32 bit per i programmi di installazione a 16 bit seguenti:

* Installazione di Microsoft per Windows 1.2  
* Installazione di Microsoft per Windows 2.6  
* Installazione di Microsoft per Windows 3.0  
* Installazione di Microsoft per Windows 3.01  
* InstallShield 5.x  

L'elenco delle sostituzioni viene archiviato nel Registro di sistema nella chiave seguente: **HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Questo meccanismo viene fornito solo per la compatibilità con le applicazioni a 32 bit che usano i programmi di installazione Microsoft a 16 bit elencati in questo argomento. L'aggiunta di programmi di installazione di terze parti non è supportata.

 

> [!Note]  
> Questo meccanismo non è incluso in Windows 10 arm.

 

 

 