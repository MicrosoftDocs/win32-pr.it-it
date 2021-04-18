---
description: 'Per ottenere un handle per un volume da utilizzare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione CreateFile con il parametro lpFileName impostato su una stringa nel formato seguente: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Ottenere un handle del volume per le operazioni del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319063"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="428d4-103">Ottenere un handle del volume per le operazioni del journal delle modifiche</span><span class="sxs-lookup"><span data-stu-id="428d4-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="428d4-104">Per ottenere un handle per un volume da utilizzare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il parametro *lpFileName* impostato su una stringa nel formato seguente: \\ \\ . \\ *X*:</span><span class="sxs-lookup"><span data-stu-id="428d4-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="428d4-105">Si noti che *X* è la lettera che identifica l'unità in cui viene visualizzato il volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="428d4-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="428d4-106">Se il volume non dispone di una lettera di unità, utilizzare la sintassi descritta in [denominazione di un volume](naming-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="428d4-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



