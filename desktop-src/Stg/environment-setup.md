---
title: Configurazione dell'ambiente
description: Il Software Development Kit (SDK) della piattaforma installata fornisce un file di Setenv.bat che si trova nella directory radice di Platform SDK, che è possibile eseguire per configurare l'ambiente per la compilazione di applicazioni che utilizzano Platform SDK.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298067"
---
# <a name="environment-setup"></a>Configurazione dell'ambiente

Il Software Development Kit (SDK) della piattaforma installata fornisce un file di Setenv.bat che si trova nella directory radice di Platform SDK, che è possibile eseguire per configurare l'ambiente per la compilazione di applicazioni che utilizzano Platform SDK.

## <a name="settings-and-variables"></a>Impostazioni e variabili

È anche possibile configurare manualmente l'ambiente aggiungendo un valore simile al seguente al file di Autoexec.bat. Utilizzando Windows, è possibile modificare il file di Autoexec.bat per includere questi comandi. Utilizzando Windows Server 2003, Windows XP, Windows 2000 o Windows NT, è possibile modificare o aggiungere queste impostazioni alle variabili di ambiente utilizzando la finestra di dialogo sistema che è possibile eseguire dal pannello di controllo.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Queste impostazioni sono appropriate per una piattaforma Intel 80386 o successiva che esegue Windows me, Windows 98 o Windows 95 con Microsoft Visual C++ e Platform SDK installati. Ad esempio, in questo sistema Visual C++ versione 5,0 viene installata nella directory C: \\ MSDEV Platform SDK viene installato nella directory D: \\ MSSDK La configurazione del disco può essere diversa. Le directory di Platform SDK (per questo esempio, quelle con D: \\ MSSDK) si trovano tutte in precedenza in ogni sequenza di percorsi. In questa sequenza si presuppone che le compilazioni da riga di comando siano eseguite nella finestra del prompt dei comandi e che i file di libreria con estensione h includano e. lib in Platform SDK siano preferiti per tali compilazioni.

La variabile di ambiente CPU è definita per controllare le compilazioni Win32, a seconda della piattaforma. I valori possibili correnti includono i386, MIPS, ALPHA e PPC. Per ulteriori informazioni, vedere il file Win32. MAK fornito in Platform SDK nella directory di \\ \\ inclusione MSSDK. Tutti i makefile di esempio di codice dell'esercitazione COM includono Win32. mak.

 

 




