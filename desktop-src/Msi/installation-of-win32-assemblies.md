---
description: Installare gli assembly Win32 rendendoli un componente del pacchetto microsoft Windows Installer che installa o aggiorna l'applicazione.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installazione di assembly Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c680d53e1c4702bab3b9a24920b18a2fdb644a86c41207712ec3726a310a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633841"
---
# <a name="installation-of-win32-assemblies"></a>Installazione di assembly Win32

Installare gli assembly Win32 rendendoli un componente del pacchetto microsoft Windows Installer che installa o aggiorna l'applicazione. Quando si crea la [tabella MsiAssembly e](msiassembly-table.md) [la tabella MsiAssemblyName](msiassemblyname-table.md), il componente nella colonna Componente viene identificato \_ come assembly. Il programma di installazione imposta la [**proprietà MsiWin32AssemblySupport**](msiwin32assemblysupport.md) sulla versione del file di Sxs.dll nei sistemi operativi in grado di supportare gli assembly Win32 e non imposta questa proprietà in caso contrario.

In Windows Vista e Windows XP, Windows installer non scrive le informazioni sugli assembly nel Registro di sistema. È anche possibile usare assembly condivisi, assembly privati e assembly side-by-side. Per informazioni, vedere [Assembly condivisi](shared-assemblies.md), [Assembly privati](private-assemblies.md)e Assembly [side-by-side](side-by-side-assemblies.md).

Le sezioni seguenti descrivono come creare un pacchetto del programma di installazione di Windows per installare assembly Win32 come condivisi, privati o side-by-side in sistemi operativi Windows diversi.

-   [Installazione di assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installazione di assembly Win32 per l'uso privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



