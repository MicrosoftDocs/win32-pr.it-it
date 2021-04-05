---
description: Durante l'installazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installazione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753767"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="897a7-104">Installazione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="897a7-104">Installation of Isolated Components</span></span>

<span data-ttu-id="897a7-105">Durante l'installazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati.</span><span class="sxs-lookup"><span data-stu-id="897a7-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="897a7-106">In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.</span><span class="sxs-lookup"><span data-stu-id="897a7-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="897a7-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="897a7-107">Installation</span></span>

-   <span data-ttu-id="897a7-108">Copiare i file di componente \_ condivisi nella stessa cartella dell'applicazione componente \_ solo se è in \_ corso l'installazione dell'applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="897a7-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="897a7-109">Creare un file di zero byte con il nome breve del file di chiave dell'applicazione componente \_ .</span><span class="sxs-lookup"><span data-stu-id="897a7-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="897a7-110">Individuare il file nella stessa cartella dell'applicazione componente \_ .</span><span class="sxs-lookup"><span data-stu-id="897a7-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="897a7-111">Aggiungere l'estensione. LOCALE con questo nome file.</span><span class="sxs-lookup"><span data-stu-id="897a7-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="897a7-112">Incrementare il refcount SharedDLL se il bit msidbComponentAttributesSharedDllRefCount è impostato nella colonna attributi della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="897a7-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="897a7-113">Registrare \_ l'applicazione componente come client del componente \_ condiviso e registrare un percorso della chiave che punta al percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="897a7-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="897a7-114">Installare tutte le risorse dell'applicazione componente \_ come di consueto.</span><span class="sxs-lookup"><span data-stu-id="897a7-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="897a7-115">Se il componente \_ condiviso o il relativo file di chiave è già installato nel computer, non copiare i file nel percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="897a7-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="897a7-116">Se il componente \_ condiviso o il relativo file di chiave non è ancora installato nel computer:</span><span class="sxs-lookup"><span data-stu-id="897a7-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="897a7-117">Copiare i file del componente \_ condiviso nel percorso condiviso.</span><span class="sxs-lookup"><span data-stu-id="897a7-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="897a7-118">Elabora tutte le azioni di installazione per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="897a7-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="897a7-119">Se Component \_ Shared è un componente com, registrare il percorso com completo in modo che la sintassi \[ $Component \] e \[ \# FileKey \] puntino al percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="897a7-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



