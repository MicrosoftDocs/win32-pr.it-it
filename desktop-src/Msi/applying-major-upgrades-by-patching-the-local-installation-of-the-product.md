---
description: Un aggiornamento principale può essere applicato a un'applicazione mediante l'applicazione di patch all'installazione locale dell'applicazione dalla riga di comando o tramite un eseguibile.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881126"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="626ca-103">Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto</span><span class="sxs-lookup"><span data-stu-id="626ca-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="626ca-104">Un aggiornamento principale può essere applicato a un'applicazione mediante l'applicazione di patch all'installazione locale dell'applicazione dalla riga di comando o tramite un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="626ca-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="626ca-105">Non è consigliabile fornire un aggiornamento principale come pacchetto di patch, perché un pacchetto di patch di aggiornamento principale non può essere sequenziato con altri aggiornamenti e perché la patch non è [installabile](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="626ca-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="626ca-106">Non è possibile usare l'utilità [Msimsp.exe](msimsp-exe.md) per generare un pacchetto di patch che applica un aggiornamento principale.</span><span class="sxs-lookup"><span data-stu-id="626ca-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="626ca-107">In alternativa, applicare gli aggiornamenti principali, come descritto in [applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="626ca-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="626ca-108">**Per applicare una patch di aggiornamento principale a un'installazione locale del prodotto**</span><span class="sxs-lookup"><span data-stu-id="626ca-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="626ca-109">Avviare l'installazione della patch dalla riga di comando o usando un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="626ca-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="626ca-110">Per avviare dalla riga di comando, usare msiexec/p patch. msp.</span><span class="sxs-lookup"><span data-stu-id="626ca-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="626ca-111">Per avviare da un eseguibile, chiamare [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o il [**Metodo ApplyPatch**](installer-applypatch.md) e fornire gli stessi argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="626ca-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="626ca-112">Quando si applica una patch a un'installazione client, il programma di installazione ignora l'origine dell'installazione e procede con la patch dei file già installati nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="626ca-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="626ca-113">Il programma di installazione modifica tutti i componenti patch contrassegnati come Run-from-source per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="626ca-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="626ca-114">Gli utenti non sono in grado di eseguire questi componenti dall'origine a condizione che la patch rimanga nel computer.</span><span class="sxs-lookup"><span data-stu-id="626ca-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="626ca-115">Il programma di installazione aggiunge qualsiasi trasformazione utilizzata per aggiornare il file con estensione msi o aggiunge informazioni specifiche della patch al profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="626ca-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="626ca-116">Il programma di installazione memorizza nella cache il file con estensione msi nel computer dell'utente, in modo da poter eseguire l'installazione su richiesta, reinstallare e ripristinare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="626ca-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="626ca-117">Dopo che una patch è stata applicata a un'installazione autonoma, il programma di installazione fa riferimento a due o più elenchi di origine a file esterni: uno per l'origine originale e uno per ogni patch che è stata applicata.</span><span class="sxs-lookup"><span data-stu-id="626ca-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



