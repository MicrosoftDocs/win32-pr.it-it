---
title: Eliminazione di utenti su server membri e Windows 2000 Professional
description: In questo argomento viene illustrato come eliminare un utente da un server membro o da un computer che esegue Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- utenti AD, eliminazione di un utente nei server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, eliminazione di utenti su server membri e Windows 2000 Professional
- eliminazione di un utente
- Server, eliminazione di un utente
- eliminazione di utenti su server membri e Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046524"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="4b1c3-108">Eliminazione di utenti su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b1c3-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="4b1c3-109">In questo argomento viene illustrato come eliminare un utente da un server membro o da un computer che esegue Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="4b1c3-110">**Per eliminare un utente**</span><span class="sxs-lookup"><span data-stu-id="4b1c3-110">**To delete a user**</span></span>

1.  <span data-ttu-id="4b1c3-111">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b1c3-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="4b1c3-112">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="4b1c3-113">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="4b1c3-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="4b1c3-114">Il &lt; parametro "nome computer &gt; " è il nome del computer di cui si desidera accedere ai gruppi.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="4b1c3-115">Questo parametro notifica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="4b1c3-116">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="4b1c3-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="4b1c3-117">Specificare "User" come classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) per eliminare l'utente.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="4b1c3-118">Tenere presente che non è necessario chiamare [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit della modifica nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="4b1c3-119">La chiamata a [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) consente di eseguire il commit dell'eliminazione dell'utente direttamente nella directory.</span><span class="sxs-lookup"><span data-stu-id="4b1c3-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 