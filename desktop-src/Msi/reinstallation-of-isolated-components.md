---
description: Durante la reinstallazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstallazione dei componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881473"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="97661-104">Reinstallazione dei componenti isolati</span><span class="sxs-lookup"><span data-stu-id="97661-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="97661-105">Durante la reinstallazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati.</span><span class="sxs-lookup"><span data-stu-id="97661-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="97661-106">In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.</span><span class="sxs-lookup"><span data-stu-id="97661-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="97661-107">Reinstallazione</span><span class="sxs-lookup"><span data-stu-id="97661-107">Reinstallation</span></span>

-   <span data-ttu-id="97661-108">Reinstallare i file del componente \_ condivisi nella stessa cartella dell' \_ applicazione Component solo se \_ viene reinstallata anche l'applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="97661-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="97661-109">Non incrementare l'elenco client di componenti \_ condivisi e non incrementare il numero di SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="97661-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="97661-110">Ricreare il file di zero byte con il nome breve del file di chiave dell'applicazione componente \_ .</span><span class="sxs-lookup"><span data-stu-id="97661-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="97661-111">Questo file deve trovarsi nella stessa cartella dell'applicazione componente \_ e avere l'estensione. Locale.</span><span class="sxs-lookup"><span data-stu-id="97661-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="97661-112">Reinstallare tutte le risorse dell'applicazione componente \_ come di consueto.</span><span class="sxs-lookup"><span data-stu-id="97661-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="97661-113">Se il refcount SharedDLL per il componente \_ condiviso è maggiore di 1 o se altri prodotti rimangono nell'elenco client di componenti \_ condivisi:</span><span class="sxs-lookup"><span data-stu-id="97661-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="97661-114">Non reinstallare alcun file nel percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="97661-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="97661-115">Se il refcount SharedDLL per il componente \_ condiviso è uguale a 1 o se non sono presenti altri client rimanenti del componente \_ condiviso:</span><span class="sxs-lookup"><span data-stu-id="97661-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="97661-116">Reinstallare i file del componente \_ condivisi nel percorso condiviso usando le regole di [controllo delle versioni dei file](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="97661-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="97661-117">Elabora tutte le azioni di reinstallazione per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="97661-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="97661-118">Se Component \_ Shared è un componente com, registrare il percorso com completo in modo che le sintassi del \[ programma \] di installazione $Component e \[ \# FileKey \] puntino al percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="97661-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



