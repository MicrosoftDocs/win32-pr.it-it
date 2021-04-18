---
description: In questo esempio viene illustrato come creare un'installazione basata su URL di un pacchetto di Windows Installer.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Esempio di installazione di Windows Installer basata su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322012"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Esempio di installazione di Windows Installer basata su Windows

In questo esempio viene illustrato come creare un'installazione basata su URL di un pacchetto di Windows Installer. Per ulteriori informazioni sulla protezione delle installazioni e sull'utilizzo di certificati digitali, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).

Per riprodurre questo esempio, è necessaria l'utilità [SignTool](../seccrypto/signtool.md) . Per informazioni dettagliate, vedere la Guida di [riferimento agli strumenti CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) in Microsoft Windows Software Development Kit (SDK). Sono inoltre necessari [Msistuff.exe](msistuff-exe.md) e Setup.exe utilità dei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Per ulteriori informazioni, vedere [bootstrap di download Internet](internet-download-bootstrapping.md).

Nell'esempio sono presenti le specifiche seguenti:

-   Quando gli utenti visitano il sito Web e fanno clic sul collegamento "installazione di configurazione", viene visualizzata l'opzione per salvare o eseguire da tale percorso. Se l'utente sceglie di eseguire da tale posizione, il Setup.exe aggiorna la versione di Windows Installer nel computer, se necessario, verifica la firma digitale nel pacchetto del programma di installazione e installa il pacchetto nel computer.
-   È disponibile un certificato digitale, ovvero cert. cer, fornito con una chiave privata, CERT. PVK.
-   L'URL del sito Web ipotetico che un cliente visita per installare il pacchetto è https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   Il layout del server Web è il seguente. 

    | URL                                                               | File        | Descrizione                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Programma di avvio automatico Setup.exe.                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | Pacchetto di installazione                           |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | File CAB di origine \# 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | File CAB di origine \# 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/Instmsi/ANSI    | Instmsi.exe | ANSI Windows Installer 2,0 ridistribuibile.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/Instmsi/Unicode | Instmsi.exe | Unicode Windows Installer 2,0 ridistribuibile. |

    

     

[Continua](configuring-the-setup-exe-resources.md)

 

 
