---
title: Creazione di utenti su server membri e Windows 2000 Professional
description: Questo argomento descrive i passaggi usati per creare un utente in un server membro o in un computer che esegue Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Creazione di utenti su server membri e Windows 2000 Professional AD
- utenti AD, creazione di un utente su server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, creazione di un utente su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046532"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="0b178-106">Creazione di utenti su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0b178-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="0b178-107">**Per creare un utente**</span><span class="sxs-lookup"><span data-stu-id="0b178-107">**To create a user**</span></span>

1.  <span data-ttu-id="0b178-108">Eseguire l'associazione al computer utilizzando le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b178-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="0b178-109">Utilizzare un account con diritti sufficienti per accedere a tale computer.</span><span class="sxs-lookup"><span data-stu-id="0b178-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="0b178-110">Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="0b178-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="0b178-111">Il &lt; computer "nome computer &gt; " è il nome del computer di cui si desidera accedere ai gruppi.</span><span class="sxs-lookup"><span data-stu-id="0b178-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="0b178-112">Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.</span><span class="sxs-lookup"><span data-stu-id="0b178-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="0b178-113">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="0b178-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="0b178-114">Specificare "User" come classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere l'utente.</span><span class="sxs-lookup"><span data-stu-id="0b178-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="0b178-115">Scrivere l'utente nel database di sicurezza del computer utilizzando [**IADs. seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="0b178-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 