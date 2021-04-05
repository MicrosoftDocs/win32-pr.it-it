---
title: Enumerazione degli utenti su server membri e Windows 2000 Professional
description: In questo argomento viene illustrato come enumerare tutti gli utenti, in un database di sicurezza locale, su server membri e computer che eseguono Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerazione degli utenti su server membri e Windows 2000 Professional AD
- utenti AD, enumerazione di utenti su server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, enumerazione di utenti su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724551"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="8d19a-106">Enumerazione degli utenti su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d19a-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="8d19a-107">In questo argomento viene illustrato come enumerare tutti gli utenti, in un database di sicurezza locale, su server membri e computer che eseguono Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8d19a-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="8d19a-108">**Per enumerare gli utenti**</span><span class="sxs-lookup"><span data-stu-id="8d19a-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="8d19a-109">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d19a-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="8d19a-110">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="8d19a-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="8d19a-111">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="8d19a-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="8d19a-112">Il &lt; parametro "nome computer &gt; " è il nome del computer per cui si desidera accedere ai gruppi.</span><span class="sxs-lookup"><span data-stu-id="8d19a-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="8d19a-113">Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="8d19a-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="8d19a-114">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="8d19a-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="8d19a-115">Aggiungere "User" alla proprietà [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="8d19a-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="8d19a-116">In questo modo l'enumerazione conterrà solo oggetti con la classe di oggetti "User".</span><span class="sxs-lookup"><span data-stu-id="8d19a-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="8d19a-117">Enumerare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="8d19a-117">Enumerate the objects.</span></span> <span data-ttu-id="8d19a-118">Per ogni oggetto utente, usare i metodi di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) per leggere le proprietà utente.</span><span class="sxs-lookup"><span data-stu-id="8d19a-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 