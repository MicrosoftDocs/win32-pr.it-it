---
description: ICE64 verifica che le nuove directory nel profilo utente vengano rimosse correttamente negli scenari di roaming.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529586"
---
# <a name="ice64"></a><span data-ttu-id="9403f-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="9403f-103">ICE64</span></span>

<span data-ttu-id="9403f-104">ICE64 verifica che le nuove directory nel profilo utente vengano rimosse correttamente negli scenari di roaming.</span><span class="sxs-lookup"><span data-stu-id="9403f-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="9403f-105">Se non si corregge un avviso o un errore segnalato da ICE64, in genere si verificano problemi nella pulizia completa del computer durante una disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="9403f-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="9403f-106">Quando un utente comune che ha installato l'applicazione accede a un computer per la prima volta, tutto il profilo viene copiato nel computer.</span><span class="sxs-lookup"><span data-stu-id="9403f-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="9403f-107">Nell'annuncio (che si verifica dopo il download del profilo mobile), il programma di installazione verifica che la directory sia già presente e pertanto non la Elimina durante la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="9403f-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="9403f-108">Questa operazione lascia la directory nel computer dell'utente in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="9403f-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="9403f-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="9403f-109">Result</span></span>

<span data-ttu-id="9403f-110">ICE64 Invia un avviso o un errore in una situazione di roaming se una nuova directory nel profilo utente da rimuovere non viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="9403f-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="9403f-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9403f-111">Example</span></span>

<span data-ttu-id="9403f-112">ICE64 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="9403f-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="9403f-113">La cartella ' MyOtherFolder ' è una cartella del profilo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9403f-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="9403f-114">Poiché non è elencato nella tabella RemoveFile, non viene rimosso in alcuni scenari.</span><span class="sxs-lookup"><span data-stu-id="9403f-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="9403f-115">Per correggere l'errore, creare una riga per la cartella nella tabella RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="9403f-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="9403f-116">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="9403f-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="9403f-117">Directory</span><span class="sxs-lookup"><span data-stu-id="9403f-117">Directory</span></span>     | <span data-ttu-id="9403f-118">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="9403f-118">Directory\_Parent</span></span> | <span data-ttu-id="9403f-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="9403f-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="9403f-120">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="9403f-120">AppDataFolder</span></span> | <span data-ttu-id="9403f-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="9403f-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="9403f-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="9403f-122">MyFolder</span></span>      | <span data-ttu-id="9403f-123">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="9403f-123">AppDataFolder</span></span>     | <span data-ttu-id="9403f-124">DataFolder</span><span class="sxs-lookup"><span data-stu-id="9403f-124">DataFolder</span></span>  |
| <span data-ttu-id="9403f-125">MyOtherFolder</span><span class="sxs-lookup"><span data-stu-id="9403f-125">MyOtherFolder</span></span> | <span data-ttu-id="9403f-126">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="9403f-126">AppDataFolder</span></span>     | <span data-ttu-id="9403f-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="9403f-127">DataFolder2</span></span> |



 

[<span data-ttu-id="9403f-128">Tabella RemoveFile</span><span class="sxs-lookup"><span data-stu-id="9403f-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="9403f-129">FileKey</span><span class="sxs-lookup"><span data-stu-id="9403f-129">FileKey</span></span> | <span data-ttu-id="9403f-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="9403f-130">Component\_</span></span> | <span data-ttu-id="9403f-131">FileName</span><span class="sxs-lookup"><span data-stu-id="9403f-131">FileName</span></span> | <span data-ttu-id="9403f-132">DirProperty</span><span class="sxs-lookup"><span data-stu-id="9403f-132">DirProperty</span></span> | <span data-ttu-id="9403f-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="9403f-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="9403f-134">Chiave1</span><span class="sxs-lookup"><span data-stu-id="9403f-134">Key1</span></span>    | <span data-ttu-id="9403f-135">Component1</span><span class="sxs-lookup"><span data-stu-id="9403f-135">Component1</span></span>  |          | <span data-ttu-id="9403f-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="9403f-136">MyFolder</span></span>    | <span data-ttu-id="9403f-137">2</span><span class="sxs-lookup"><span data-stu-id="9403f-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="9403f-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9403f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9403f-139">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="9403f-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



