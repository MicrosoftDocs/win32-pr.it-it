---
title: Configurazione dell'ambiente
description: Platform Software Development Kit (SDK) installato fornisce un file Setenv.bat che si trova nella directory radice di Platform SDK che è possibile eseguire per configurare l'ambiente per la compilazione di applicazioni che usano Platform SDK.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b7de27bfc015726786011376c821c5ae0e86a07d95f03098ed376dd022cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739391"
---
# <a name="environment-setup"></a>Configurazione dell'ambiente

Platform Software Development Kit (SDK) installato fornisce un file Setenv.bat che si trova nella directory radice di Platform SDK che è possibile eseguire per configurare l'ambiente per la compilazione di applicazioni che usano Platform SDK.

## <a name="settings-and-variables"></a>Impostazioni variabili e

È anche possibile configurare manualmente l'ambiente aggiungendo qualcosa di simile al seguente al file Autoexec.bat file. Usando Windows, è possibile modificare il file Autoexec.bat per includere questi comandi. Usando Windows Server 2003, Windows XP, Windows 2000 o Windows NT, è possibile modificare o aggiungere queste impostazioni alle variabili di ambiente usando la finestra di dialogo Sistema che è possibile eseguire dal Pannello di controllo.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Queste impostazioni sono appropriate per una piattaforma Intel 80386 o successiva che esegue Windows Me, Windows 98 o Windows 95 con Microsoft Visual C++ e Platform SDK installato. In questo sistema, ad esempio, Visual C++ versione 5.0 viene installata nella directory C: \\ MSDEV. Platform SDK viene installato nella directory D: \\ MSSDK. La configurazione del disco potrebbe essere diversa. Le directory di Platform SDK (per questo esempio, quelle in cui sono presenti D: MSSDK) sono tutte precedenti \\ in ogni sequenza di percorso. Questa sequenza presuppone che le compilazioni da riga di comando siano destinate all'esecuzione nella finestra del prompt dei comandi e che i file di libreria con estensione h include e lib in Platform SDK siano preferiti per tali compilazioni.

La variabile di ambiente CPU viene definita per controllare le compilazioni Win32, a seconda della piattaforma. I valori possibili correnti includono i386, MIPS, ALPHA e PPC. Per altre informazioni, vedere il file Win32.mak fornito in Platform SDK nella \\ directory MSSDK \\ INCLUDE. Tutti i makefile di esempio dell'esercitazione COM includono Win32.mak.

 

 




