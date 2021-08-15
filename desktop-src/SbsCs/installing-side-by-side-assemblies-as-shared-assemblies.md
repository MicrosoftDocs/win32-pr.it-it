---
description: La procedura seguente descrive come installare assembly side-by-side come assembly condivisi.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installazione di assembly side-by-side come assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127511"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installazione di assembly side-by-side come assembly condivisi

La procedura seguente descrive come installare [assembly side-by-side](about-side-by-side-assemblies-.md) come [assembly condivisi.](/windows/desktop/Msi/shared-assemblies)

**Per installare un assembly side-by-side come assembly condiviso**

1.  Firmare e creare un catalogo per i file nell'assembly.

    I file devono essere firmati per installarli come assembly side-by-side. Per altre informazioni, vedere [Creazione di cataloghi e file firmati](creating-signed-files-and-catalogs.md).

2.  È consigliabile installare assembly side-by-side condivisi come componenti di un pacchetto Windows Installer. Può trattarsi dello stesso pacchetto di installazione usato per installare o aggiornare l'applicazione. Se l'assembly condiviso viene fornito come parte di più applicazioni, è necessario fornire un modulo unione che può essere incorporato nei pacchetti di installazione di queste applicazioni e creare un catalogo per i file nell'assembly.

    Windows Per installare gli assembly è necessaria la versione 2.0 o successiva del programma di installazione. Per altre informazioni, vedere l'SDK [Windows Installer](../msi/windows-installer-portal.md) e le sezioni in Installazione di [assembly Win32](../msi/installation-of-win32-assemblies.md).

 

 
