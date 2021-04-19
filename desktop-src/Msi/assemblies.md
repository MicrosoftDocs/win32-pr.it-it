---
description: Windows Installer possibile installare, rimuovere e aggiornare gli assembly e gli assembly Win32 utilizzati dall'Common Language Runtime di Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311052"
---
# <a name="assemblies"></a>Assembly

Windows Installer possibile installare, rimuovere e aggiornare gli assembly e gli assembly Win32 utilizzati dall'Common Language Runtime di Microsoft .NET Framework. Un assembly viene gestito dal Windows Installer come un singolo componente del programma di installazione. Tutti i file che costituiscono un assembly devono essere contenuti in un singolo componente del programma di installazione elencato nella tabella dei [componenti](component-table.md) .

Windows Installer eseguiti in Windows Vista e Windows XP possono installare assembly affiancati. Gli assembly affiancati possono condividere in modo sicuro gli assembly tra più applicazioni e possono compensare gli effetti negativi della condivisione degli assembly, ad esempio i conflitti tra DLL. Anziché una singola versione di un assembly che presuppone la compatibilità con le versioni precedenti di tutte le applicazioni, la condivisione di assembly affiancati consente l'esecuzione simultanea di più versioni di un assembly COM o Win32 nel sistema. Questa funzionalità migliorata per isolare le applicazioni è una parte importante del Framework Microsoft .NET. Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Nelle sezioni seguenti viene descritto l'utilizzo degli assembly con il Windows Installer.

-   [Aggiunta di assembly a un pacchetto](adding-assemblies-to-a-package.md)
-   [Installazione e rimozione di assembly](installing-and-removing-assemblies.md)
-   [Aggiornamento degli assembly](updating-assemblies.md)
-   [Modalità di reinstallazione degli assembly Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Chiavi del registro di sistema dell'assembly scritte da Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)

Per informazioni sull'installazione di applicazioni COM e COM+ 1,0, vedere [installazione di un'applicazione com+ con il Windows Installer](installing-a-com--application-with-the-windows-installer.md), [installazione di un componente com in un percorso privato](installing-a-com-component-to-a-private-location.md)e [rendere privato un componente com in un pacchetto esistente](make-a-com-component-in-an-existing-package-private.md).

 

 
