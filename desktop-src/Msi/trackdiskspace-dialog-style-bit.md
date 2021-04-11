---
description: Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit di stile della finestra di dialogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128110"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="1c934-103">Bit di stile della finestra di dialogo TrackDiskSpace</span><span class="sxs-lookup"><span data-stu-id="1c934-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="1c934-104">Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="1c934-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="1c934-105">Se la proprietà viene modificata, viene inviata una notifica ai controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1c934-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="1c934-106">Questo stile può essere utilizzato se è presente un controllo nella finestra di dialogo che indica lo spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="1c934-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="1c934-107">Se l'utente passa a un'altra applicazione, aggiunge o rimuove file o modifica in altro modo lo spazio su disco disponibile, è possibile implementare rapidamente la modifica usando questo stile.</span><span class="sxs-lookup"><span data-stu-id="1c934-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="1c934-108">Qualsiasi finestra di dialogo che si basa sulla proprietà [**OutOfDiskSpace**](outofdiskspace.md) per determinare se visualizzare una finestra di dialogo deve impostare il bit di stile della finestra di dialogo TrackDiskSpace per la finestra di dialogo per aggiornare in modo dinamico lo spazio sui volumi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c934-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="1c934-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1c934-109">Value</span></span>



| <span data-ttu-id="1c934-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="1c934-110">Decimal</span></span> | <span data-ttu-id="1c934-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="1c934-111">Hexadecimal</span></span> | <span data-ttu-id="1c934-112">Costante</span><span class="sxs-lookup"><span data-stu-id="1c934-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="1c934-113">32</span><span class="sxs-lookup"><span data-stu-id="1c934-113">32</span></span>      | <span data-ttu-id="1c934-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="1c934-114">0x00000020</span></span>  | <span data-ttu-id="1c934-115">**msidbDialogAttributesTrackDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="1c934-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



