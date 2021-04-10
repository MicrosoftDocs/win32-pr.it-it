---
description: È possibile applicare il piccolo aggiornamento a un'installazione locale di MNP2000 con la patch di esempio MNPpatch. msp creata per generare un pacchetto di patch.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Applicazione di un pacchetto di patch a un'installazione locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227215"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="a639a-103">Applicazione di un pacchetto di patch a un'installazione locale</span><span class="sxs-lookup"><span data-stu-id="a639a-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="a639a-104">È possibile applicare il piccolo aggiornamento a un'installazione locale di MNP2000 con la patch di esempio MNPpatch. msp creata per [generare un pacchetto di patch](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="a639a-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="a639a-105">La procedura generale è illustrata nella sezione [applicazione di piccoli aggiornamenti applicando patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="a639a-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="a639a-106">Installare il prodotto MNP2000 originale localmente nel computer.</span><span class="sxs-lookup"><span data-stu-id="a639a-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="a639a-107">Verificare che sia presente l'errore Concert.txt che la correzione del piccolo aggiornamento sia stata completata.</span><span class="sxs-lookup"><span data-stu-id="a639a-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="a639a-108">Avviare quindi l'installazione immettendo la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="a639a-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="a639a-109">**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**</span><span class="sxs-lookup"><span data-stu-id="a639a-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="a639a-110">Esaminare nuovamente i Concert.txt appartenenti a MNP2000 per verificare che il programma di installazione abbia applicato il piccolo aggiornamento per correggere il file.</span><span class="sxs-lookup"><span data-stu-id="a639a-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="a639a-111">Per applicare il piccolo aggiornamento a un'immagine amministrativa, vedere [applicazione di un pacchetto di patch a un'installazione amministrativa](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="a639a-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="a639a-112">Continua</span><span class="sxs-lookup"><span data-stu-id="a639a-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 



