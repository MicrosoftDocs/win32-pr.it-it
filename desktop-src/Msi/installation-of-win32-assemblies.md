---
description: Installare gli assembly Win32 rendendoli un componente di Microsoft Windows Installer pacchetto che installa o aggiorna l'applicazione.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installazione degli assembly Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308898"
---
# <a name="installation-of-win32-assemblies"></a>Installazione degli assembly Win32

Installare gli assembly Win32 rendendoli un componente di Microsoft Windows Installer pacchetto che installa o aggiorna l'applicazione. Quando si creano la tabella [MsiAssembly](msiassembly-table.md) e la [tabella MsiAssemblyName](msiassemblyname-table.md), il componente viene identificato \_ come assembly nella colonna Component. Il programma di installazione imposterà la proprietà [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) sulla versione del file di Sxs.dll nei sistemi operativi che possono supportare gli assembly Win32 senza impostare questa proprietà in caso contrario.

In Windows Vista e Windows XP, Windows Installer non scrive informazioni sull'assembly nel registro di sistema. È inoltre possibile utilizzare assembly condivisi, assembly privati e assembly affiancati. Per informazioni, vedere assembly [condivisi](shared-assemblies.md), [assembly privati](private-assemblies.md)e [assembly side-by-side](side-by-side-assemblies.md).

Nelle sezioni seguenti viene descritto come creare un pacchetto di Windows Installer per installare assembly Win32 come condiviso, privato o affiancato in diversi sistemi operativi Windows.

-   [Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



