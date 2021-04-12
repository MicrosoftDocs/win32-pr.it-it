---
title: Applicazione desktop di esempio
description: Applicazione desktop di esempio
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- applicazione di esempio WMDMApp
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396087"
---
# <a name="sample-desktop-application"></a>Applicazione desktop di esempio

Windows Media Gestione dispositivi viene fornito con un'applicazione desktop di esempio denominata WMDMApp. Questa applicazione dispone di un'interfaccia utente grafica che consente di esplorare i dispositivi connessi, creare playlist nel dispositivo e trascinare i file multimediali nel dispositivo.

Questa applicazione di esempio è costituita da due parti:

-   wmdapp.exe, un eseguibile che visualizza una finestra ed esegue la maggior parte dell'interfaccia utente e della funzionalità di base del programma e
-   proghelp.dll, una DLL helper che esegue funzioni di utilità per l'applicazione. È necessario registrare questa DLL dopo la compilazione del progetto.

Per compilare l'applicazione di esempio, è possibile usare Visual Studio. Nella sezione seguente viene descritto come eseguire questa operazione:

-   [Compilazione dell'applicazione di esempio con Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Dopo aver compilato il progetto, registrare il file di proghelp.dll. Per registrare questa DLL, aprire un prompt dei comandi e passare alla directory contenente questa DLL e digitare `regsvr32 proghelp.dll` .

 

 




