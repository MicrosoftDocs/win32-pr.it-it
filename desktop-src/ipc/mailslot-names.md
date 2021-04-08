---
description: Denominazione di mailslot e inserimento di messaggi in mailslot.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomi inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749687"
---
# <a name="mailslot-names"></a><span data-ttu-id="6d933-103">Nomi inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="6d933-103">Mailslot Names</span></span>

<span data-ttu-id="6d933-104">Quando un processo crea un inserimento/espulsione, il nome inserimento/espulsione deve avere il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="6d933-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="6d933-105">\\\\.\\ \\ \[  \\ \] *nome* percorso inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="6d933-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="6d933-106">Un nome inserimento/espulsione richiede gli elementi seguenti: due barre rovesciate per iniziare il nome, un punto, una barra rovesciata che segue il punto, la parola "inserimento/espulsione" e una barra rovesciata finale.</span><span class="sxs-lookup"><span data-stu-id="6d933-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="6d933-107">I nomi non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6d933-107">Names are not case sensitive.</span></span> <span data-ttu-id="6d933-108">Un nome inserimento/espulsione può essere preceduto da un percorso costituito dai nomi di una o più directory, separate da barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="6d933-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="6d933-109">Se, ad esempio, un utente prevede che i messaggi siano soggetti a imposte da Bob, Pete e querela, l'applicazione inserimento/espulsione dell'utente potrebbe consentire all'utente di creare singoli mailslot per ogni mittente, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6d933-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="6d933-110">\\\\.\\ Commenti su inserimento/espulsione \\ imposte \\ Bob \_</span><span class="sxs-lookup"><span data-stu-id="6d933-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="6d933-111">\\\\.\\ inserimento/espulsione \\ imposte \\ Petes \_</span><span class="sxs-lookup"><span data-stu-id="6d933-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="6d933-112">\\\\.\\ inserimento/espulsione \\ le imposte \\ causa \_ Commenti</span><span class="sxs-lookup"><span data-stu-id="6d933-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="6d933-113">Per inserire un messaggio in un inserimento/espulsione, un processo apre un inserimento/espulsione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6d933-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="6d933-114">Per scrivere in un inserimento/espulsione nel computer locale, un processo può usare un nome di inserimento/espulsione con lo stesso formato usato per la creazione di un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="6d933-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="6d933-115">Questa situazione, tuttavia, è relativamente insolita.</span><span class="sxs-lookup"><span data-stu-id="6d933-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="6d933-116">Con maggiore frequenza, utilizzare il seguente formato per scrivere in un inserimento/espulsione in un computer remoto specifico:</span><span class="sxs-lookup"><span data-stu-id="6d933-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="6d933-117">\\\\*Nomecomputer* \\ \\ \[  \\ \] *nome* percorso inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="6d933-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="6d933-118">Per inserire un messaggio in ogni inserimento/espulsione del dominio specificato con un nome specificato, utilizzare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="6d933-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="6d933-119">\\\\*NomeDominio* \\ \\ \[  \\ \] *nome* percorso inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="6d933-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="6d933-120">Per inserire un messaggio in ogni inserimento/espulsione con un nome specificato nel dominio primario del sistema, usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="6d933-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="6d933-121">\\\\\*\\\\ \[  \\ \] *nome* percorso inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="6d933-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



