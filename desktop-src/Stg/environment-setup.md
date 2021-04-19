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
# <a name="environment-setup"></a><span data-ttu-id="443cc-103">Configurazione dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="443cc-103">Environment Setup</span></span>

<span data-ttu-id="443cc-104">Il Software Development Kit (SDK) della piattaforma installata fornisce un file di Setenv.bat che si trova nella directory radice di Platform SDK, che è possibile eseguire per configurare l'ambiente per la compilazione di applicazioni che utilizzano Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="443cc-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="443cc-105">Impostazioni e variabili</span><span class="sxs-lookup"><span data-stu-id="443cc-105">Settings and Variables</span></span>

<span data-ttu-id="443cc-106">È anche possibile configurare manualmente l'ambiente aggiungendo un valore simile al seguente al file di Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="443cc-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="443cc-107">Utilizzando Windows, è possibile modificare il file di Autoexec.bat per includere questi comandi.</span><span class="sxs-lookup"><span data-stu-id="443cc-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="443cc-108">Utilizzando Windows Server 2003, Windows XP, Windows 2000 o Windows NT, è possibile modificare o aggiungere queste impostazioni alle variabili di ambiente utilizzando la finestra di dialogo sistema che è possibile eseguire dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="443cc-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="443cc-109">Queste impostazioni sono appropriate per una piattaforma Intel 80386 o successiva che esegue Windows me, Windows 98 o Windows 95 con Microsoft Visual C++ e Platform SDK installati.</span><span class="sxs-lookup"><span data-stu-id="443cc-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="443cc-110">Ad esempio, in questo sistema Visual C++ versione 5,0 viene installata nella directory C: \\ MSDEV</span><span class="sxs-lookup"><span data-stu-id="443cc-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="443cc-111">Platform SDK viene installato nella directory D: \\ MSSDK</span><span class="sxs-lookup"><span data-stu-id="443cc-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="443cc-112">La configurazione del disco può essere diversa.</span><span class="sxs-lookup"><span data-stu-id="443cc-112">Your disk configuration may be different.</span></span> <span data-ttu-id="443cc-113">Le directory di Platform SDK (per questo esempio, quelle con D: \\ MSSDK) si trovano tutte in precedenza in ogni sequenza di percorsi.</span><span class="sxs-lookup"><span data-stu-id="443cc-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="443cc-114">In questa sequenza si presuppone che le compilazioni da riga di comando siano eseguite nella finestra del prompt dei comandi e che i file di libreria con estensione h includano e. lib in Platform SDK siano preferiti per tali compilazioni.</span><span class="sxs-lookup"><span data-stu-id="443cc-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="443cc-115">La variabile di ambiente CPU è definita per controllare le compilazioni Win32, a seconda della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="443cc-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="443cc-116">I valori possibili correnti includono i386, MIPS, ALPHA e PPC.</span><span class="sxs-lookup"><span data-stu-id="443cc-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="443cc-117">Per ulteriori informazioni, vedere il file Win32. MAK fornito in Platform SDK nella directory di \\ \\ inclusione MSSDK.</span><span class="sxs-lookup"><span data-stu-id="443cc-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="443cc-118">Tutti i makefile di esempio di codice dell'esercitazione COM includono Win32. mak.</span><span class="sxs-lookup"><span data-stu-id="443cc-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




