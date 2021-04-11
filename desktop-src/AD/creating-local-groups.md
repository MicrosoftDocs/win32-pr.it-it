---
title: Creazione di gruppi locali
description: Per i server membri e Windows 2000 Professional è possibile creare solo gruppi locali.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creazione di gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336814"
---
# <a name="creating-local-groups"></a><span data-ttu-id="9647c-104">Creazione di gruppi locali</span><span class="sxs-lookup"><span data-stu-id="9647c-104">Creating Local Groups</span></span>

<span data-ttu-id="9647c-105">Per i server membri e Windows 2000 Professional è possibile creare solo gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="9647c-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="9647c-106">**Per creare un gruppo locale per un server membro o un computer che esegue Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="9647c-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="9647c-107">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="9647c-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="9647c-108">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="9647c-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="9647c-109">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="9647c-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="9647c-110">Il &lt; parametro "nome computer &gt; " è il nome dei gruppi di computer a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="9647c-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="9647c-111">Nella stringa di binding il parametro " &lt; computer &gt; " indica a ADSI che è associato a un computer.</span><span class="sxs-lookup"><span data-stu-id="9647c-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="9647c-112">ADSI rende questi dati disponibili per il parser del provider WinNT in modo che possa ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="9647c-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="9647c-113">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="9647c-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="9647c-114">Specificare "localGroup" come classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere il gruppo.</span><span class="sxs-lookup"><span data-stu-id="9647c-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="9647c-115">Se si specifica "Group" come classe, ADSI USA "localGroup".</span><span class="sxs-lookup"><span data-stu-id="9647c-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="9647c-116">Non specificare la classe come "globalGroup".</span><span class="sxs-lookup"><span data-stu-id="9647c-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="9647c-117">Non è possibile creare gruppi della classe "globalGroup" nei server membro o in un computer che esegue Windows NT Workstation/Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9647c-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="9647c-118">Se si specifica "globalGroup", [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea il gruppo nella cache delle proprietà, ma [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) non scrive il gruppo nel database di sicurezza e non restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9647c-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="9647c-119">Scrivere il gruppo nel database di sicurezza del computer utilizzando [**IADs. seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="9647c-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 