---
description: Questo esempio illustra come localizzare il pacchetto di Windows Installer descritto in un esempio di installazione. Il pacchetto di installazione originale viene modificato da una versione in lingua inglese a quella francese.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Esempio di localizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311104"
---
# <a name="a-localization-example"></a><span data-ttu-id="74f57-104">Esempio di localizzazione</span><span class="sxs-lookup"><span data-stu-id="74f57-104">A Localization Example</span></span>

<span data-ttu-id="74f57-105">Questo esempio illustra come localizzare il pacchetto di Windows Installer descritto in [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="74f57-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="74f57-106">Il pacchetto di installazione originale viene modificato da una versione in lingua inglese a quella francese.</span><span class="sxs-lookup"><span data-stu-id="74f57-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="74f57-107">L'esempio di localizzazione presenta le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="74f57-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="74f57-108">L'interfaccia utente di installazione per l'applicazione MNP2000 deve essere modificata da inglese a francese.</span><span class="sxs-lookup"><span data-stu-id="74f57-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="74f57-109">La versione francese di MNP2000 include Readme.txt e Help.txt file scritti in lingua francese.</span><span class="sxs-lookup"><span data-stu-id="74f57-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="74f57-110">La versione francese include un elenco di agenti di viaggio in Francia che possono fornire biglietti a Red Park Arena.</span><span class="sxs-lookup"><span data-stu-id="74f57-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="74f57-111">Questo elenco (fornito come nuovo file, Fre.txt) non fa parte della versione in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="74f57-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="74f57-112">La procedura generale per la localizzazione di un'installazione di è descritta nella sezione [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="74f57-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="74f57-113">Copiare la versione in lingua inglese di MNP2000.msi e tutti i file di origine descritti in [pianificazione dell'installazione](planning-the-installation.md) in una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="74f57-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="74f57-114">Modificare il nome del MNP2000.msi nella cartella MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="74f57-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="74f57-115">Nelle sezioni seguenti verrà modificata questa copia per localizzare l'applicazione in francese.</span><span class="sxs-lookup"><span data-stu-id="74f57-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="74f57-116">Continua</span><span class="sxs-lookup"><span data-stu-id="74f57-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



