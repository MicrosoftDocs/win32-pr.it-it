---
description: Un'installazione amministrativa crea un'immagine di origine di un'applicazione o di un prodotto in una rete.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967286"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="847bb-103">Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa</span><span class="sxs-lookup"><span data-stu-id="847bb-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="847bb-104">Un' [installazione amministrativa](administrative-installation.md) crea un'immagine di origine di un'applicazione o di un prodotto in una rete.</span><span class="sxs-lookup"><span data-stu-id="847bb-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="847bb-105">Gli utenti di un gruppo di lavoro che hanno accesso a questa immagine amministrativa possono installare il prodotto da questa origine.</span><span class="sxs-lookup"><span data-stu-id="847bb-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="847bb-106">L'aggiornamento dell'applicazione per questo gruppo di lavoro viene eseguito in due passaggi:</span><span class="sxs-lookup"><span data-stu-id="847bb-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="847bb-107">Per prima cosa, è possibile applicare la patch di aggiornamento di piccole dimensioni all'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="847bb-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="847bb-108">In secondo luogo, le modifiche apportate al piccolo aggiornamento devono essere propagate agli utenti.</span><span class="sxs-lookup"><span data-stu-id="847bb-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="847bb-109">**Per applicare una patch di aggiornamento di piccole dimensioni a un'immagine amministrativa**</span><span class="sxs-lookup"><span data-stu-id="847bb-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="847bb-110">Ottenere il piccolo aggiornamento sotto forma di pacchetto di [patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="847bb-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="847bb-111">Ad esempio, il piccolo aggiornamento denominato patch. msp.</span><span class="sxs-lookup"><span data-stu-id="847bb-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="847bb-112">Ottenere il percorso dell'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="847bb-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="847bb-113">Dalla riga di comando usare:</span><span class="sxs-lookup"><span data-stu-id="847bb-113">From the command line use:</span></span>

    <span data-ttu-id="847bb-114">**msiexec/a** *\[ percorso del file \] di immagine amministrativa. msi* **/p** *patch. msp*</span><span class="sxs-lookup"><span data-stu-id="847bb-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="847bb-115">Vengono aggiornati i file dell'applicazione e il file con estensione msi dell'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="847bb-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="847bb-116">Per un elenco delle opzioni che è possibile usare con Msiexec.exe, vedere [Opzioni della riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="847bb-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="847bb-117">Windows Installer determina automaticamente se l'immagine amministrativa utilizza nomi di file brevi e imposta la proprietà [**SHORTFILENAMES**](shortfilenames.md) .</span><span class="sxs-lookup"><span data-stu-id="847bb-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="847bb-118">L'immagine amministrativa risultante è identica a quella generata da un'installazione amministrativa usando un CD-ROM di prodotto completo che include l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="847bb-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="847bb-119">Quando i nuovi utenti installano l'applicazione da questa origine ricevono l'applicazione aggiornata.</span><span class="sxs-lookup"><span data-stu-id="847bb-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="847bb-120">**Per propagare il piccolo aggiornamento al gruppo di lavoro**</span><span class="sxs-lookup"><span data-stu-id="847bb-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="847bb-121">I membri del gruppo di lavoro ottengono le modifiche reinstallando l'applicazione dall'immagine amministrativa utilizzando la procedura descritta in [applicazione di piccoli aggiornamenti tramite la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="847bb-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



