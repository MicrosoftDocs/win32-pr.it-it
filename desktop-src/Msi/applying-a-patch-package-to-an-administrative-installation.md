---
description: È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000. msp creata in generazione di un pacchetto di patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Applicazione di un pacchetto di patch a un'installazione amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967288"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="91514-103">Applicazione di un pacchetto di patch a un'installazione amministrativa</span><span class="sxs-lookup"><span data-stu-id="91514-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="91514-104">È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000. msp creata in [generazione di un pacchetto di patch](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="91514-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="91514-105">L'aggiornamento può quindi essere propagato agli utenti richiedendo la reinstallazione dell'applicazione dalla nuova immagine di origine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="91514-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="91514-106">Un amministratore può usare la riga di comando seguente per aggiornare l'immagine di origine amministrativa situata in//server/MNP2000.msi a una nuova immagine di origine che corrisponde a quella generata da un'installazione amministrativa da un CD-ROM completamente aggiornato.</span><span class="sxs-lookup"><span data-stu-id="91514-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="91514-107">**msiexec/a//server/MNP2000.msi/p MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="91514-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="91514-108">I membri del gruppo di lavoro che usa MNP2000 devono reinstallare l'applicazione dalla nuova immagine di origine amministrativa per ricevere l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="91514-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="91514-109">Per reinstallare completamente le applicazioni e memorizzare nella cache il file con estensione msi aggiornato nel computer dell'utente, è possibile che gli utenti immettano uno dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91514-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="91514-110">**msiexec/fvomus//server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="91514-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="91514-111">**msiexec/I//server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="91514-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="91514-112">Per reinstallare solo la funzionalità di concerto aggiornata e memorizzare nella cache il file con estensione msi aggiornato nel computer dell'utente, è possibile che gli utenti immettano il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="91514-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="91514-113">**msiexec/I//server/MNP2000.msi REINSTALL = Concert REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="91514-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="91514-114">Esempio successivo</span><span class="sxs-lookup"><span data-stu-id="91514-114">Next example</span></span>

[<span data-ttu-id="91514-115">Esempio di localizzazione</span><span class="sxs-lookup"><span data-stu-id="91514-115">A Localization Example</span></span>](a-localization-example.md)

 

 



