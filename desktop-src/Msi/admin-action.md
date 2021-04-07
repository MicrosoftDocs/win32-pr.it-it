---
description: L'azione di amministrazione è un'azione di primo livello utilizzata per eseguire installazioni amministrative.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Azione di amministrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881153"
---
# <a name="admin-action"></a><span data-ttu-id="2549d-103">Azione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="2549d-103">ADMIN Action</span></span>

<span data-ttu-id="2549d-104">L'azione di amministrazione è un'azione di primo livello utilizzata per eseguire [installazioni amministrative](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="2549d-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2549d-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="2549d-105">Sequence Restrictions</span></span>

<span data-ttu-id="2549d-106">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="2549d-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2549d-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="2549d-107">ActionData Messages</span></span>

<span data-ttu-id="2549d-108">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="2549d-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="2549d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2549d-109">Remarks</span></span>

<span data-ttu-id="2549d-110">L'azione di amministrazione non viene chiamata dalla sequenza della tabella delle azioni, Windows Installer esegue questa azione quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *szCommandLine* impostato su "Action = admin" o l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando "/a".</span><span class="sxs-lookup"><span data-stu-id="2549d-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2549d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2549d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2549d-112">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="2549d-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="2549d-113">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2549d-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



