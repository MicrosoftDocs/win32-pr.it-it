---
description: Se un pacchetto di Windows Installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel registro di sistema locale.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Chiavi del registro di sistema dell'assembly scritte da Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528867"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Chiavi del registro di sistema dell'assembly scritte da Windows Installer

Se un pacchetto di Windows Installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel registro di sistema locale. Si noti che queste chiavi del registro di sistema sono destinate esclusivamente all'uso interno da Windows Installer e non devono essere basate sull'applicazione. Il contenuto, la posizione e la struttura delle informazioni archiviate in queste chiavi sono soggette a modifiche. Le applicazioni devono basarsi su [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per gestire gli assembly.

Gli assembly vengono registrati con i rispettivi nomi di assembly. I nomi dei valori archiviati nei percorsi seguenti sono i nomi degli assembly. I valori effettivi sono di tipo REG \_ \_ multisz e contengono i dati utilizzati da [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per installare o ripristinare gli assembly.

## <a name="information-about-private-assemblies"></a>Informazioni sugli assembly privati

Windows Installer archivia le informazioni sugli assembly privati trasportati dai pacchetti Windows Installer installati come applicazioni per utente gestite con la seguente chiave del registro di sistema:

**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programma di installazione** \\ **Gestione** \\ di **SID *_\\_* utente** Percorso assembly del programma di installazione del \\  \\ * *_file di configurazione_* _

Windows Installer archivia le informazioni sugli assembly privati trasferiti da Windows Installer pacchetti installati per utente con la seguente chiave del registro di sistema:

_***\\** Percorso degli **\\** **\\** assembly di Microsoft Installer per HKCU Software per il **\\** **\\** _file di configurazione_*_

Windows Installer archivia le informazioni sugli assembly privati trasferiti dai pacchetti Windows Installer e installati per computer con la seguente chiave del registro di sistema:

_***\\** Percorso degli **\\** assembly del programma di installazione delle classi Software HKLM **\\** **\\** **\\** _al file di configurazione_*_

## <a name="information-about-global-or-shared-assemblies"></a>Informazioni sugli assembly globali o condivisi

Windows Installer archivia le informazioni sugli assembly condivisi trasportati dai pacchetti Windows Installer installati come applicazioni per utente gestite con la seguente chiave del registro di sistema:

_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User SID_*_ \\ _ *installazione **\\** assembly **\\** globali**

Windows Installer archivia le informazioni sugli assembly condivisi trasferiti dai pacchetti Windows Installer installati per utente con la seguente chiave del registro di sistema:

**HKCU** \\ **Software** \\ di **Microsoft** \\ **Programma di installazione** \\ **Assembly** \\ **Globali**

Windows Installer archivia le informazioni sugli assembly condivisi trasferiti dai pacchetti Windows Installer e installati per computer con la seguente chiave del registro di sistema:

**HKLM** \\ **Software** \\ di **Classi** \\ **Programma di installazione** \\ **Assembly** \\ **Globali**

 

 



