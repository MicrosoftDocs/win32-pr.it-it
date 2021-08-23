---
description: Se un Windows installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel Registro di sistema locale.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Chiavi del Registro di sistema degli assembly scritte dal Windows di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fd4a9bf3fa5e1eb557c2a179ec3e9a0853149ff197922a9fbf633a2869f41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746021"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Chiavi del Registro di sistema degli assembly scritte dal Windows di installazione

Se un Windows installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel Registro di sistema locale. Si noti che queste chiavi del Registro di sistema devono essere usate solo internamente da Windows Installer e non devono essere usate dall'applicazione. Il contenuto, la posizione e la struttura delle informazioni archiviate in queste chiavi sono soggetti a modifiche. Le applicazioni devono [**basarsi su MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per gestire gli assembly.

Gli assembly vengono registrati in base ai relativi nomi di assembly. I nomi dei valori archiviati nei percorsi seguenti sono i nomi degli assembly. I valori effettivi sono di tipo REG MULTI SZ e contengono i dati usati \_ \_ da [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per installare o ripristinare gli assembly.

## <a name="information-about-private-assemblies"></a>Informazioni sugli assembly privati

Windows Il programma di installazione archivia le informazioni sugli assembly privati trasportati da pacchetti di Windows Installer installati come applicazioni gestite per utente nella chiave del Registro di sistema seguente:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programma di installazione** \\ **Gestito** \\ **_SID utente_ *_\\_* Percorso** \\ **degli assembly del** programma di installazione al file di \\ **_configurazione_**

Windows Il programma di installazione archivia le informazioni sugli assembly privati Windows pacchetti del programma di installazione installati per utente nella chiave del Registro di sistema seguente:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Programma di installazione** \\ **Assembly** \\ **_percorso del file di configurazione_**

Windows Il programma di installazione archivia le informazioni sugli assembly privati trasportati Windows pacchetti del programma di installazione e installati per computer nella chiave del Registro di sistema seguente:

**HKLM** \\ **SOFTWARE** \\ **Classi** \\ **Programma di installazione** \\ **Assembly** \\ **_percorso del file di configurazione_**

## <a name="information-about-global-or-shared-assemblies"></a>Informazioni sugli assembly globali o condivisi

Windows Il programma di installazione archivia le informazioni sugli assembly condivisi Windows pacchetti del programma di installazione installati come applicazioni gestite per utente nella chiave del Registro di sistema seguente:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programma di installazione** \\ **Gestito** \\ **_SID utente_ *_\\_* Assembly** \\ **del programma di installazione** \\ **globali**

Windows Il programma di installazione archivia le informazioni sugli assembly condivisi Windows pacchetti del programma di installazione installati per utente nella chiave del Registro di sistema seguente:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Programma di installazione** \\ **Assembly** \\ **Globale**

Windows Il programma di installazione archivia le informazioni sugli assembly condivisi Windows pacchetti del programma di installazione e installati per computer nella chiave del Registro di sistema seguente:

**HKLM** \\ **SOFTWARE** \\ **Classi** \\ **Programma di installazione** \\ **Assembly** \\ **Globale**

 

 



