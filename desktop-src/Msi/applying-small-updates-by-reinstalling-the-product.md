---
description: Un piccolo aggiornamento può essere applicato a un'applicazione eseguendo una reinstallazione completa o parziale dell'applicazione dalla riga di comando o da un programma.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967284"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="ffea0-103">Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="ffea0-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="ffea0-104">Un piccolo aggiornamento può essere applicato a un'applicazione eseguendo una reinstallazione completa o parziale dell'applicazione dalla riga di comando o da un programma.</span><span class="sxs-lookup"><span data-stu-id="ffea0-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="ffea0-105">**Per propagare il piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) dalla riga di comando**</span><span class="sxs-lookup"><span data-stu-id="ffea0-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="ffea0-106">Dalla riga di comando usare: **msiexec/fvomus \[** _percorso del file con estensione msi aggiornato_ *_\]_* o **msiexec/i \[** _percorso al file MSI aggiornato_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.</span><span class="sxs-lookup"><span data-stu-id="ffea0-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="ffea0-107">Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ffea0-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="ffea0-108">Si noti che l'utente non può reinstallare il prodotto utilizzando Installazione applicazioni perché il file con estensione msi aggiornato non è ancora presente nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ffea0-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="ffea0-109">**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) da un programma**</span><span class="sxs-lookup"><span data-stu-id="ffea0-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="ffea0-110">Da un programma, chiamare [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e specificare il \_ pacchetto REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ UserData e il \_ collegamento REINSTALLMODE</span><span class="sxs-lookup"><span data-stu-id="ffea0-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="ffea0-111">Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ffea0-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="ffea0-112">Il metodo seguente avvia una reinstallazione solo delle funzionalità o dei componenti interessati dall'aggiornamento di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="ffea0-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="ffea0-113">**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione parziale)**</span><span class="sxs-lookup"><span data-stu-id="ffea0-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="ffea0-114">Ottenere un elenco dei nomi delle funzionalità e dei componenti interessati dall'aggiornamento di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="ffea0-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="ffea0-115">Dal prompt dei comandi usare: **msiexec/i \[** _percorso di aggiornamento del file con estensione msi_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.</span><span class="sxs-lookup"><span data-stu-id="ffea0-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="ffea0-116">Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ffea0-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



