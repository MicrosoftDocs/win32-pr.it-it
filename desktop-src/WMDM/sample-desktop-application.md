---
title: Applicazione desktop di esempio
description: Applicazione desktop di esempio
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Device Manager, esempio di applicazione desktop
- Gestione dispositivi, esempio di applicazione desktop
- Applicazione di esempio wmdmapp
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e8037ccf963f26637711cd6d0e77ea7d2b4ff3cede72fcbded6600226d36c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584248"
---
# <a name="sample-desktop-application"></a>Applicazione desktop di esempio

Il Windows Gestione dispositivi multimediali viene fornito con un'applicazione desktop di esempio denominata wmdmapp. Questa applicazione ha un'interfaccia utente grafica che consente di esplorare i dispositivi connessi, creare playlist nel dispositivo e trascinare i file multimediali nel dispositivo.

Questa applicazione di esempio è costituita da due parti:

-   wmdapp.exe, un eseguibile che visualizza una finestra ed esegue la maggior parte dell'interfaccia utente e delle funzionalità di base del programma e
-   proghelp.dll, una DLL helper che esegue funzioni di utilità per l'applicazione. È necessario registrare questa DLL dopo la compilazione del progetto.

Per compilare l'applicazione di esempio, è possibile usare Visual Studio. La sezione seguente descrive come eseguire questa operazione:

-   [Compilazione dell'applicazione di esempio tramite Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Dopo aver compilato il progetto, registrare il proghelp.dll file. Per registrare questa DLL, aprire un prompt dei comandi e passare alla directory contenente la DLL e digitare `regsvr32 proghelp.dll` .

 

 




