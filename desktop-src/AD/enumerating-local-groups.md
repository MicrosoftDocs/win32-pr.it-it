---
title: Enumerazione dei gruppi locali
description: Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è possibile enumerare tutti i gruppi locali.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724554"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="943fe-104">Enumerazione dei gruppi locali</span><span class="sxs-lookup"><span data-stu-id="943fe-104">Enumerating Local Groups</span></span>

<span data-ttu-id="943fe-105">Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è possibile enumerare tutti i gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="943fe-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="943fe-106">Nei server membri e in Windows 2000 Professional è possibile creare solo gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="943fe-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="943fe-107">Tuttavia, tali gruppi locali possono contenere:</span><span class="sxs-lookup"><span data-stu-id="943fe-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="943fe-108">Gruppi universali e globali dalla foresta che contiene il dominio al quale appartiene il computer.</span><span class="sxs-lookup"><span data-stu-id="943fe-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="943fe-109">Gruppi locali di dominio dal dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="943fe-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="943fe-110">Utenti di qualsiasi dominio nella foresta.</span><span class="sxs-lookup"><span data-stu-id="943fe-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="943fe-111">**Per enumerare i gruppi locali in un server membro o in un computer che esegue Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="943fe-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="943fe-112">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="943fe-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="943fe-113">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="943fe-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="943fe-114">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="943fe-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="943fe-115">Il parametro "The <computer name> " è il nome del gruppo di computer a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="943fe-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="943fe-116">Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="943fe-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="943fe-117">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="943fe-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="943fe-118">Impostare un filtro che contenga "gruppi" utilizzando la proprietà [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="943fe-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="943fe-119">In questo modo è possibile enumerare il contenitore e recuperare solo i gruppi.</span><span class="sxs-lookup"><span data-stu-id="943fe-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="943fe-120">Enumerare gli oggetti Group usando il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="943fe-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="943fe-121">Per ogni oggetto gruppo, utilizzare l'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) per leggere il nome e i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="943fe-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 