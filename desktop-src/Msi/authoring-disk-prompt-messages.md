---
description: Usare le linee guida seguenti per creare un'installazione di Windows Installer che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creazione di messaggi di richiesta del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311045"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="3ab8f-103">Creazione di messaggi di richiesta del disco</span><span class="sxs-lookup"><span data-stu-id="3ab8f-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="3ab8f-104">Usare le linee guida seguenti per creare un'installazione di Windows Installer che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.</span><span class="sxs-lookup"><span data-stu-id="3ab8f-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="3ab8f-105">**Per visualizzare una finestra di messaggio che richiede all'utente di inserire un disco**</span><span class="sxs-lookup"><span data-stu-id="3ab8f-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="3ab8f-106">Utilizzare le funzionalità di creazione del programma di installazione per impostare la stringa di proprietà [**DiskPrompt**](diskprompt.md) nella tabella delle [Proprietà](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab8f-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="3ab8f-107">Deve includere il nome del prodotto da installare e un parametro segnaposto nella stringa per il titolo stampato sul disco.</span><span class="sxs-lookup"><span data-stu-id="3ab8f-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="3ab8f-108">Per Microsoft Publisher, ad esempio, la proprietà **DiskPrompt** potrebbe essere "Microsoft Publisher: disk \[ 1 \] ", dove \[ 1 \] è il segnaposto per il titolo del disco.</span><span class="sxs-lookup"><span data-stu-id="3ab8f-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="3ab8f-109">Immettere i titoli di ogni disco richiesto in righe separate della colonna DiskPrompt della tabella [media](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab8f-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="3ab8f-110">Ad esempio, la prima e unica voce nella tabella media potrebbe essere "1 – Install".</span><span class="sxs-lookup"><span data-stu-id="3ab8f-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="3ab8f-111">Durante l'azione [InstallFiles](installfiles-action.md) , il valore della colonna DiskPrompt della tabella [supporti](media-table.md) sostituisce il segnaposto nella stringa della proprietà [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab8f-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="3ab8f-112">Il messaggio visualizzato dalla finestra di messaggio viene creato da una stringa di modello predefinita nella tabella degli [errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="3ab8f-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="3ab8f-113">Si tratta dell'errore 1302 e della stringa di modello: "inserire il disco: \[ 2 \] " e \[ 2 \] rappresenta un segnaposto per la proprietà [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab8f-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="3ab8f-114">Nell'esempio viene visualizzato il messaggio seguente all'utente: "inserire il disco: Microsoft Publisher: disco 1 – install."</span><span class="sxs-lookup"><span data-stu-id="3ab8f-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="3ab8f-115">Si noti che i messaggi di richiesta del disco vengono visualizzati da tutti i [livelli di interfaccia utente](user-interface-levels.md) tranne nessuno.</span><span class="sxs-lookup"><span data-stu-id="3ab8f-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



