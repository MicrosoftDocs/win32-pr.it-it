---
description: Un eseguibile di bootstrap configurabile (Setup.exe) e uno strumento di configurazione (Msistuff.exe) sono inclusi nei componenti di Windows SDK per gli sviluppatori Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configurazione delle risorse Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322041"
---
# <a name="configuring-the-setupexe-resources"></a>Configurazione delle risorse Setup.exe

Un eseguibile di bootstrap configurabile (Setup.exe) e uno strumento di configurazione ( [Msistuff.exe](msistuff-exe.md)) sono inclusi nei [componenti di Windows SDK per gli sviluppatori Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Utilizzando Msistuff.exe per configurare le risorse in Setup.exe, gli sviluppatori possono creare facilmente un'installazione Web di un pacchetto di Windows Installer. Per ulteriori informazioni, vedere [bootstrap di download Internet](internet-download-bootstrapping.md).

Immettendo la seguente riga di comando vengono configurate le risorse per l'esempio descritto in [un URL basato Windows Installer esempio di installazione](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continua](sign-setup-exe-and-mysetup-msi.md)

 

 



