---
description: Windows Il programma di installazione può installare, rimuovere e aggiornare assembly Win32 e assembly usati da Common Language Runtime di Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a228dfad8155b9282f7ed5ee5c288a858f55c74c432ec6d21fd98aae58f98472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639273"
---
# <a name="assemblies"></a>Assembly

Windows Il programma di installazione può installare, rimuovere e aggiornare assembly Win32 e assembly usati da Common Language Runtime di Microsoft .NET Framework. Un assembly viene gestito dal programma di installazione di Windows come singolo componente del programma di installazione. Tutti i file che costituiscono un assembly devono essere contenuti in un singolo componente del programma di installazione elencato nella [tabella Componente.](component-table.md)

Windows Il programma di installazione Windows Vista e Windows XP possono installare assembly side-by-side. Gli assembly side-by-side possono condividere in modo sicuro gli assembly tra più applicazioni e possono compensare gli effetti negativi della condivisione di assembly, ad esempio i conflitti di DLL. Anziché una singola versione di un assembly che presuppone la compatibilità con le versioni precedenti di tutte le applicazioni, la condivisione di assembly side-by-side consente l'esecuzione simultanea di più versioni di un assembly COM o Win32 nel sistema. Questa funzionalità migliorata per isolare le applicazioni è una parte importante di Microsoft .NET Framework. Per altre informazioni, vedere Applicazioni isolate e [assembly side-by-side.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

Le sezioni seguenti descrivono l'uso di assembly con il Windows di installazione.

-   [Aggiunta di assembly a un pacchetto](adding-assemblies-to-a-package.md)
-   [Installazione e rimozione di assembly](installing-and-removing-assemblies.md)
-   [Aggiornamento degli assembly](updating-assemblies.md)
-   [Modalità di reinstallazione degli assembly Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Chiavi del Registro di sistema degli assembly scritte Windows programma di installazione](assembly-registry-keys-written-by-windows-installer-.md)

Per informazioni sull'installazione di applicazioni COM e COM+ 1.0, vedere Installazione di un'applicazione [COM+](installing-a-com--application-with-the-windows-installer.md)con il programma di installazione di Windows , Installazione di un componente [COM](installing-a-com-component-to-a-private-location.md)in un percorso privato e Rendere privato un componente COM in un pacchetto [esistente.](make-a-com-component-in-an-existing-package-private.md)

 

 
