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
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="70a8b-103">Download di un'installazione da Internet</span><span class="sxs-lookup"><span data-stu-id="70a8b-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="70a8b-104">Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="70a8b-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="70a8b-105">Windows Installer possibile installare pacchetti, patch e trasformazioni da un percorso URL.</span><span class="sxs-lookup"><span data-stu-id="70a8b-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="70a8b-106">Se il database di installazione si trova in un URL, il programma di installazione scaricherà il database in un percorso della cache prima di avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="70a8b-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="70a8b-107">Il programma di installazione Scarica anche i file e i file CAB da Internet source appropriati per le selezioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="70a8b-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="70a8b-108">Per ulteriori informazioni, vedere [l'esempio di installazione di Windows Installer basato su URL](a-url-based-windows-installer-installation-example.md) .</span><span class="sxs-lookup"><span data-stu-id="70a8b-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="70a8b-109">Per installare un pacchetto con un'origine che si trova in un server Web in, ad esempio https://server/share/package.msi , è possibile utilizzare le opzioni della [riga di comando](command-line-options.md) per installare il pacchetto e impostare le proprietà [pubbliche](public-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="70a8b-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="70a8b-110">msiexec/i https://server/share/package.msi *Property = valore*</span><span class="sxs-lookup"><span data-stu-id="70a8b-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="70a8b-111">Una riga di comando simile a quella illustrata in precedenza deve essere passata al programma di installazione per avviare un'installazione da un Web browser.</span><span class="sxs-lookup"><span data-stu-id="70a8b-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="70a8b-112">In generale, non è consigliabile scaricare e installare il pacchetto semplicemente facendo doppio clic sul file con estensione msi dall'interno del browser.</span><span class="sxs-lookup"><span data-stu-id="70a8b-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="70a8b-113">Viene scaricato il file con estensione msi nella cartella Temporary Internet Files e il comando seguente viene passato al programma di installazione:</span><span class="sxs-lookup"><span data-stu-id="70a8b-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="70a8b-114">**msiexec/i c: \\ \\ file Internet temporanei di Windows \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="70a8b-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="70a8b-115">L'installazione ha esito negativo se il pacchetto richiede file di origine esterni o file CAB perché non si trovano nello stesso percorso del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="70a8b-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="70a8b-116">Si noti che poiché l'oggetto del [**programma di installazione**](installer-object.md) non è contrassegnato come [SafeForScripting](safeforscripting.md) nel computer dell'utente, gli utenti devono modificare le impostazioni di sicurezza del browser affinché l'esempio funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="70a8b-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="70a8b-117">Il metodo [**InstallProduct**](installer-installproduct.md) può essere usato per eseguire il comando precedente da un browser come un evento di clic.</span><span class="sxs-lookup"><span data-stu-id="70a8b-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


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



<span data-ttu-id="70a8b-118">Si noti che poiché alcuni server Web fanno distinzione tra maiuscole e minuscole, il campo FileName della tabella [file](file-table.md) deve corrispondere esattamente al caso dei file di origine per garantire il supporto dei download su Internet.</span><span class="sxs-lookup"><span data-stu-id="70a8b-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="70a8b-119">Vedere [download e installazione di una patch da Internet](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="70a8b-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="70a8b-120">Per ulteriori informazioni sulla protezione delle installazioni e sull'utilizzo di certificati digitali, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="70a8b-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="70a8b-121">Per ulteriori informazioni su come creare un'installazione Web di un pacchetto di Windows Installer, vedere [bootstrap download Internet](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="70a8b-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="70a8b-122">Protocolli Internet disponibili</span><span class="sxs-lookup"><span data-stu-id="70a8b-122">Available Internet Protocols</span></span>

<span data-ttu-id="70a8b-123">A partire da Windows Server 2003 e Windows XP, il programma di installazione può usare i protocolli HTTP, HTTPS e FILE.</span><span class="sxs-lookup"><span data-stu-id="70a8b-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="70a8b-124">Il programma di installazione non supporta i protocolli FTP e GOPHER.</span><span class="sxs-lookup"><span data-stu-id="70a8b-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="70a8b-125">Windows Installer versione 2,0 può utilizzare i protocolli HTTP, FILE e FTP e non può utilizzare i protocolli HTTPS e GOPHER.</span><span class="sxs-lookup"><span data-stu-id="70a8b-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



