---
title: Eliminazione di gruppi locali
description: In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer che esegue Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminazione di gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472603"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="3580c-104">Eliminazione di gruppi locali</span><span class="sxs-lookup"><span data-stu-id="3580c-104">Deleting Local Groups</span></span>

<span data-ttu-id="3580c-105">In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer che esegue Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3580c-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="3580c-106">**Per eliminare un gruppo locale**</span><span class="sxs-lookup"><span data-stu-id="3580c-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="3580c-107">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="3580c-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="3580c-108">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="3580c-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="3580c-109">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="3580c-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="3580c-110">Il &lt; parametro "nome computer &gt; " è il nome del gruppo di computer a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="3580c-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="3580c-111">Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="3580c-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="3580c-112">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="3580c-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="3580c-113">Specificare "Group" come classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)per eliminare il gruppo.</span><span class="sxs-lookup"><span data-stu-id="3580c-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="3580c-114">Non è necessario chiamare [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit della modifica nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="3580c-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="3580c-115">La chiamata a [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) consente di eseguire il commit dell'eliminazione del gruppo direttamente nella directory.</span><span class="sxs-lookup"><span data-stu-id="3580c-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 