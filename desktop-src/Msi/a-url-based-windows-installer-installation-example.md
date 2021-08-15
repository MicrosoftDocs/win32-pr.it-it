---
description: Questo esempio illustra come creare un'installazione basata su URL di un pacchetto Windows Installer.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Esempio di installazione di Windows Installer basata su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c25fb4f84ff3507505be7f16675b8da39afd349cb1b4c78520ee3de004df749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013329"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Esempio di installazione di Windows Installer basata su Windows

Questo esempio illustra come creare un'installazione basata su URL di un pacchetto Windows Installer. Per altre informazioni sulla protezione delle installazioni e sull'uso dei certificati digitali, vedere [Linee](guidelines-for-authoring-secure-installations.md) guida per la creazione di installazioni protette e firme digitali [Windows programma di installazione.](digital-signatures-and-windows-installer.md)

Per riprodurre questo esempio è necessaria [l'utilità SignTool.](../seccrypto/signtool.md) Per informazioni dettagliate, vedere le informazioni di riferimento per gli strumenti [CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) in Microsoft Windows Software Development Kit (SDK). Sono anche necessarie [Msistuff.exe](msistuff-exe.md) e Setup.exe da [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Per altre informazioni, vedere [Bootstrap del download Internet.](internet-download-bootstrapping.md)

L'esempio presenta le specifiche seguenti:

-   Quando gli utenti visitano il sito Web e fanno clic sul collegamento "Installazione mySetup", viene visualizzata l'opzione per salvare o eseguire da tale percorso. Se l'utente sceglie di eseguire da tale percorso, il Setup.exe aggiorna la versione del programma di installazione di Windows nel computer, se necessario, verifica la firma digitale nel pacchetto del programma di installazione e installa il pacchetto nel computer.
-   È presente un certificato digitale, Mycert.cer, fornito con una chiave privata, Mycert.pvk.
-   L'URL dell'ipotetico sito Web che un cliente visiterebbe per installare il pacchetto è https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   Il layout del server Web è il seguente. 

    | URL                                                               | File        | Descrizione                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Setup.exe programma di avvio automatico.                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | Pacchetto di installazione                           |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | File CAB di origine \# 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | File CAB di origine \# 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi    | Instmsi.exe | ANSI Windows Installer 2.0 Redistributable.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2.0 Redistributable. |

    

     

[Continua](configuring-the-setup-exe-resources.md)

 

 
