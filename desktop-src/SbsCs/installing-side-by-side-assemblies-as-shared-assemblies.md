---
description: Nella procedura seguente viene descritto come installare assembly side-by-side come assembly condivisi.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installazione di assembly side-by-side come assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484644"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installazione di assembly side-by-side come assembly condivisi

Nella procedura seguente viene descritto come installare [assembly side-by-side](about-side-by-side-assemblies-.md) come [assembly condivisi](/windows/desktop/Msi/shared-assemblies).

**Per installare un assembly side-by-side come assembly condiviso**

1.  Firmare e creare un catalogo per i file nell'assembly.

    I file devono essere firmati per installarli come assembly side-by-side. Per altre informazioni, vedere [creazione di file e cataloghi firmati](creating-signed-files-and-catalogs.md).

2.  È necessario installare assembly side-by-side condivisi come componenti di un pacchetto di Windows Installer. Può trattarsi dello stesso pacchetto di installazione usato per installare o aggiornare l'applicazione. Se l'assembly condiviso viene fornito come parte di più applicazioni, è necessario fornire un modulo merge che può essere incorporato nei pacchetti di installazione di tali applicazioni e creare un catalogo per i file nell'assembly.

    Per installare gli assembly è necessario Windows Installer versione 2,0 o successiva. Per ulteriori informazioni, vedere il [Windows Installer](../msi/windows-installer-portal.md) SDK e le sezioni in [installazione degli assembly Win32](../msi/installation-of-win32-assemblies.md).

 

 
