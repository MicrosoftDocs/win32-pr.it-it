---
description: 'È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione SetVolumeMountPoint, a condizione che non sia già stato assegnato un volume a tale lettera di unità.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Assegnazione di una lettera di unità a un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310039"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="d0f74-103">Assegnazione di una lettera di unità a un volume</span><span class="sxs-lookup"><span data-stu-id="d0f74-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="d0f74-104">È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , a condizione che non sia già stato assegnato un volume a tale lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="d0f74-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="d0f74-105">Se il volume locale dispone già di una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="d0f74-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="d0f74-106">quindi [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d0f74-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="d0f74-107">Per gestire questa operazione, eliminare innanzitutto la lettera di unità utilizzando la funzione [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="d0f74-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="d0f74-108">Per un esempio di codice, vedere [modifica delle assegnazioni di lettere di unità](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="d0f74-109">Il sistema supporta al massimo una lettera di unità per ogni volume.</span><span class="sxs-lookup"><span data-stu-id="d0f74-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="d0f74-110">Pertanto, non è possibile avere C: \\ e F: \\ rappresentano lo stesso volume.</span><span class="sxs-lookup"><span data-stu-id="d0f74-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="d0f74-111">Per eliminare una lettera di unità esistente e assegnarne una nuova, è possibile che si verifichino interruzioni dei percorsi esistenti, ad esempio quelli nei collegamenti desktop.</span><span class="sxs-lookup"><span data-stu-id="d0f74-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="d0f74-112">Potrebbe inoltre interrompere il percorso del programma che rende la lettera di unità modificata.</span><span class="sxs-lookup"><span data-stu-id="d0f74-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="d0f74-113">Con la gestione della memoria virtuale di Windows, questa operazione potrebbe interrompere l'applicazione, lasciando il sistema in uno stato instabile ed eventualmente inutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="d0f74-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="d0f74-114">È responsabilità del progettista del programma evitare tali catastrofi potenziali.</span><span class="sxs-lookup"><span data-stu-id="d0f74-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



