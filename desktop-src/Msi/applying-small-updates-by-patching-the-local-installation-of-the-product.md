---
description: Un piccolo aggiornamento può essere applicato a un'applicazione applicando patch all'installazione locale dell'applicazione.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967285"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="ae1e4-103">Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto</span><span class="sxs-lookup"><span data-stu-id="ae1e4-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="ae1e4-104">Un piccolo aggiornamento può essere applicato a un'applicazione applicando patch all'installazione locale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="ae1e4-105">**Per applicare una patch di aggiornamento di piccole dimensioni a un'installazione locale del prodotto**</span><span class="sxs-lookup"><span data-stu-id="ae1e4-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="ae1e4-106">Avviare l'installazione della patch dalla riga di comando o usando un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="ae1e4-107">Per avviare dalla riga di comando, usare **msiexec/p patch. msp REINSTALL \[ =**_feature list_ *_\] REINSTALLMODE = omus_*.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="ae1e4-108">Per avviare da un eseguibile, chiamare [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o il [**Metodo ApplyPatch**](installer-applypatch.md) e fornire gli stessi argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="ae1e4-109">Quando si applica una patch a un'installazione client, il programma di installazione ignora l'origine dell'installazione e procede con la patch dei file già installati nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="ae1e4-110">Il programma di installazione modifica tutti i componenti patch contrassegnati come Run-from-source per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="ae1e4-111">Gli utenti non sono in grado di eseguire questi componenti dall'origine a condizione che la patch rimanga nel computer.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="ae1e4-112">Il programma di installazione aggiunge qualsiasi trasformazione utilizzata per aggiornare il file con estensione msi o aggiunge informazioni specifiche della patch al profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="ae1e4-113">Il programma di installazione memorizza nella cache il file con estensione msi nel computer dell'utente, in modo da poter eseguire l'installazione su richiesta, reinstallare e ripristinare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="ae1e4-114">Dopo che una patch è stata applicata a un'installazione autonoma, il programma di installazione fa riferimento a due o più elenchi di origine a file esterni: uno per l'origine originale e uno per ogni patch che è stata applicata.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



