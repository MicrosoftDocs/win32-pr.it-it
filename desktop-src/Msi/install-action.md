---
description: L'azione di installazione è un'azione di primo livello chiamata per installare o rimuovere i componenti.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Azione di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049852"
---
# <a name="install-action"></a><span data-ttu-id="6ee3f-103">Azione di installazione</span><span class="sxs-lookup"><span data-stu-id="6ee3f-103">INSTALL Action</span></span>

<span data-ttu-id="6ee3f-104">L'azione di installazione è un'azione di primo livello chiamata per installare o rimuovere i componenti.</span><span class="sxs-lookup"><span data-stu-id="6ee3f-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="6ee3f-105">Questa azione esegue una query sulla [tabella InstallUISequence](installuisequence-table.md) e sulla [tabella InstallExecuteSequence](installexecutesequence-table.md) per l'azione da eseguire, la condizione per l'esecuzione dell'azione e il posto dell'azione nella sequenza:</span><span class="sxs-lookup"><span data-stu-id="6ee3f-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6ee3f-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="6ee3f-106">Sequence Restrictions</span></span>

<span data-ttu-id="6ee3f-107">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="6ee3f-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6ee3f-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="6ee3f-108">ActionData Messages</span></span>

<span data-ttu-id="6ee3f-109">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="6ee3f-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee3f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ee3f-110">Remarks</span></span>

<span data-ttu-id="6ee3f-111">L'azione di installazione non viene chiamata dalla sequenza della tabella delle azioni, viene passata a Windows Installer quando viene chiamato [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando '**/i**' o quando viene chiamata una funzione di installazione che può eseguire un'attività di installazione, ad esempio [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="6ee3f-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



