---
description: L'azione annuncia è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Pubblicizza azione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756245"
---
# <a name="advertise-action"></a><span data-ttu-id="18372-103">Pubblicizza azione</span><span class="sxs-lookup"><span data-stu-id="18372-103">ADVERTISE Action</span></span>

<span data-ttu-id="18372-104">L'azione annuncia è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.</span><span class="sxs-lookup"><span data-stu-id="18372-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="18372-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="18372-105">Sequence Restrictions</span></span>

<span data-ttu-id="18372-106">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="18372-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="18372-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="18372-107">ActionData Messages</span></span>

<span data-ttu-id="18372-108">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="18372-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="18372-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="18372-109">Remarks</span></span>

<span data-ttu-id="18372-110">Per [*annuncio*](a-gly.md) si intende la capacità del programma di installazione di fornire le interfacce di caricamento e avvio di un'applicazione senza installare fisicamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18372-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="18372-111">Il programma di installazione non installa i componenti necessari fino a quando un utente o un'applicazione non attiva un'interfaccia annunciata.</span><span class="sxs-lookup"><span data-stu-id="18372-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="18372-112">Questo concetto viene definito [*installazione su richiesta*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="18372-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="18372-113">L'azione ADVERTISe non viene chiamata dall'interno della sequenza della tabella Action, il Windows Installer esegue questa azione quando l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando '/j ' o quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *SZCOMMANDLINE* impostato su Action = advertise.</span><span class="sxs-lookup"><span data-stu-id="18372-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18372-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18372-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18372-115">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="18372-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



