---
description: Un eseguibile bootstrap configurabile (Setup.exe) e uno strumento di configurazione (Msistuff.exe) sono inclusi in Windows SDK Components for Windows Installer Developers.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configurazione delle Setup.exe seguenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638730"
---
# <a name="configuring-the-setupexe-resources"></a>Configurazione delle Setup.exe seguenti

Un file eseguibile bootstrap configurabile (Setup.exe) e uno strumento di configurazione ( [Msistuff.exe](msistuff-exe.md)) sono inclusi in [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Usando Msistuff.exe per configurare le risorse in Setup.exe, gli sviluppatori possono creare facilmente un'installazione Web di un pacchetto Windows Installer. Per altre informazioni, vedere [Bootstrap del download Internet.](internet-download-bootstrapping.md)

Se si immette la riga di comando seguente, vengono configurate le risorse per l'esempio descritto in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continua](sign-setup-exe-and-mysetup-msi.md)

 

 



