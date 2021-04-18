---
description: Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per un'installazione.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Download di un'installazione da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309492"
---
# <a name="downloading-an-installation-from-the-internet"></a>Download di un'installazione da Internet

Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per un'installazione. Windows Installer possibile installare pacchetti, patch e trasformazioni da un percorso URL.

Se il database di installazione si trova in un URL, il programma di installazione scaricherà il database in un percorso della cache prima di avviare l'installazione. Il programma di installazione Scarica anche i file e i file CAB da Internet source appropriati per le selezioni dell'utente. Per ulteriori informazioni, vedere [l'esempio di installazione di Windows Installer basato su URL](a-url-based-windows-installer-installation-example.md) .

Per installare un pacchetto con un'origine che si trova in un server Web in, ad esempio https://server/share/package.msi , è possibile utilizzare le opzioni della [riga di comando](command-line-options.md) per installare il pacchetto e impostare le proprietà [pubbliche](public-properties.md) .

msiexec/i https://server/share/package.msi *Property = valore*

Una riga di comando simile a quella illustrata in precedenza deve essere passata al programma di installazione per avviare un'installazione da un Web browser. In generale, non è consigliabile scaricare e installare il pacchetto semplicemente facendo doppio clic sul file con estensione msi dall'interno del browser. Viene scaricato il file con estensione msi nella cartella Temporary Internet Files e il comando seguente viene passato al programma di installazione:

**msiexec/i c: \\ \\ file Internet temporanei di Windows \\package.msi**

L'installazione ha esito negativo se il pacchetto richiede file di origine esterni o file CAB perché non si trovano nello stesso percorso del file con estensione msi.

Si noti che poiché l'oggetto del [**programma di installazione**](installer-object.md) non è contrassegnato come [SafeForScripting](safeforscripting.md) nel computer dell'utente, gli utenti devono modificare le impostazioni di sicurezza del browser affinché l'esempio funzioni correttamente.

Il metodo [**InstallProduct**](installer-installproduct.md) può essere usato per eseguire il comando precedente da un browser come un evento di clic.


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



Si noti che poiché alcuni server Web fanno distinzione tra maiuscole e minuscole, il campo FileName della tabella [file](file-table.md) deve corrispondere esattamente al caso dei file di origine per garantire il supporto dei download su Internet.

Vedere [download e installazione di una patch da Internet](downloading-and-installing-a-patch-from-the-internet.md). Per ulteriori informazioni sulla protezione delle installazioni e sull'utilizzo di certificati digitali, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md). Per ulteriori informazioni su come creare un'installazione Web di un pacchetto di Windows Installer, vedere [bootstrap download Internet](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Protocolli Internet disponibili

A partire da Windows Server 2003 e Windows XP, il programma di installazione può usare i protocolli HTTP, HTTPS e FILE. Il programma di installazione non supporta i protocolli FTP e GOPHER.

Windows Installer versione 2,0 può utilizzare i protocolli HTTP, FILE e FTP e non può utilizzare i protocolli HTTPS e GOPHER.

 

 



