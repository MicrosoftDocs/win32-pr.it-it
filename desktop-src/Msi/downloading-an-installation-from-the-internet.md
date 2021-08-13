---
description: Windows Il programma di installazione accetta un Uniform Resource Locator (URL) come origine valida per un'installazione.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Download di un'installazione da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5195b0ec0e5c36e7b6866232c498c02a9f4022d207cd86cc229a49ec5a5e8bac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637768"
---
# <a name="downloading-an-installation-from-the-internet"></a>Download di un'installazione da Internet

Windows Il programma di installazione accetta un Uniform Resource Locator (URL) come origine valida per un'installazione. Windows Il programma di installazione può installare pacchetti, patch e trasformazioni da un percorso URL.

Se il database di installazione si trova in un URL, il programma di installazione scarica il database in un percorso della cache prima di avviare l'installazione. Il programma di installazione scarica anche i file e i file CAB dall'origine Internet appropriati per le selezioni dell'utente. Per [altre informazioni, vedere](a-url-based-windows-installer-installation-example.md) Windows di installazione del programma di installazione basato su URL.

Ad esempio, per installare un pacchetto con un'origine che si trova in un server Web in , è possibile usare le opzioni della riga di comando per installare il pacchetto e https://server/share/package.msi impostare le [proprietà](public-properties.md) pubbliche. [](command-line-options.md)

msiexec /i https://server/share/package.msi *PROPERTY=VALUE*

Una riga di comando simile a quella illustrata in precedenza deve essere passata al programma di installazione per avviare un'installazione da un Web browser. In generale, è consigliabile non scaricare e installare il pacchetto semplicemente facendo doppio clic sul file .msi dal browser. Il file di .msi verrà scaricato nella cartella dei file temporanei Internet e il comando seguente verrà passato al programma di installazione:

**msiexec /i c: \\ file temporanei Internet di Windows \\ \\package.msi**

L'installazione non riesce se il pacchetto richiede file o file CAB di origine esterni perché non si trovano nello stesso percorso del file .msi.

Si noti che poiché l'oggetto [**Installer**](installer-object.md) non è contrassegnato come [SafeForScripting](safeforscripting.md) nel computer dell'utente, gli utenti devono modificare le impostazioni di sicurezza del browser per il corretto funzionamento dell'esempio.

Il [**metodo InstallProduct**](installer-installproduct.md) può essere usato per eseguire il comando precedente da un browser come evento su clic.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Si noti che poiché in alcuni server Web viene fatto distinzione tra maiuscole e minuscole, il campo FileName nella tabella [File](file-table.md) deve corrispondere esattamente al caso dei file di origine per garantire il supporto dei download Internet.

Vedere [Download and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md)(Download e installazione di una patch da Internet). Per altre informazioni sulla protezione delle installazioni [](guidelines-for-authoring-secure-installations.md) e sull'uso dei certificati digitali, vedere Linee guida per la creazione di installazioni protette e firme digitali e Windows [programma di installazione.](digital-signatures-and-windows-installer.md) Per altre informazioni su come creare un'installazione Web di un pacchetto Windows Installer, vedere [Bootstrap del download Internet.](internet-download-bootstrapping.md)

## <a name="available-internet-protocols"></a>Protocolli Internet disponibili

A partire Windows Server 2003 e Windows XP, il programma di installazione può usare i protocolli HTTP, HTTPS e FILE. Il programma di installazione non supporta i protocolli FTP e GOPHER.

Windows Il programma di installazione versione 2.0 può usare i protocolli HTTP, FILE e FTP e i protocolli HTTPS e GOPHER.

 

 



