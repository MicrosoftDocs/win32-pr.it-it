---
description: Windows Installer esegue le azioni seguenti durante la rimozione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Rimozione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314781"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="43b1c-104">Rimozione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="43b1c-104">Removal of Isolated Components</span></span>

<span data-ttu-id="43b1c-105">Windows Installer esegue le azioni seguenti durante la rimozione di un'applicazione quando il pacchetto contiene componenti isolati.</span><span class="sxs-lookup"><span data-stu-id="43b1c-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="43b1c-106">In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.</span><span class="sxs-lookup"><span data-stu-id="43b1c-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="43b1c-107">Disinstallare</span><span class="sxs-lookup"><span data-stu-id="43b1c-107">Uninstall</span></span>

-   <span data-ttu-id="43b1c-108">Rimuovere i file di componente \_ condivisi dalla cartella contenente l' \_ applicazione Component solo se \_ viene rimossa anche l'applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="43b1c-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="43b1c-109">Se il bit msidbComponentAttributesSharedDllRefCount è impostato nella [tabella dei componenti](component-table.md) , decrementare SHAREDDLL refcount.</span><span class="sxs-lookup"><span data-stu-id="43b1c-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="43b1c-110">Rimuovere il. File locale di zero byte dalla cartella contenente l' \_ applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="43b1c-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="43b1c-111">Rimuovere \_ l'applicazione componente dall'elenco client di componenti \_ condivisi.</span><span class="sxs-lookup"><span data-stu-id="43b1c-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="43b1c-112">Rimuovere tutte le risorse dell'applicazione componente \_ come di consueto.</span><span class="sxs-lookup"><span data-stu-id="43b1c-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="43b1c-113">Se sono presenti altri prodotti rimanenti nell'elenco client di componenti \_ condivisi:</span><span class="sxs-lookup"><span data-stu-id="43b1c-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="43b1c-114">Rimuovere i file dal percorso condiviso del componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="43b1c-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="43b1c-115">Se il refcount SharedDLL per il componente \_ condiviso è 0 dopo essere stato decrementato oppure se non sono presenti altri client rimanenti del componente \_ condiviso:</span><span class="sxs-lookup"><span data-stu-id="43b1c-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="43b1c-116">Rimuovere i file di componente \_ condivisi dal percorso condiviso.</span><span class="sxs-lookup"><span data-stu-id="43b1c-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="43b1c-117">Elabora tutte le azioni di disinstallazione rispetto a questo componente.</span><span class="sxs-lookup"><span data-stu-id="43b1c-117">Process all uninstall actions with respect to this component.</span></span>

 

 



