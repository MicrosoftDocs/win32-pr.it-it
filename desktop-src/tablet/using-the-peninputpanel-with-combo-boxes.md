---
description: Viene descritto l'utilizzo dell'oggetto PenInputPanel con caselle combinate.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Uso di PenInputPanel con caselle combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751263"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="7c9f9-103">Uso di PenInputPanel con caselle combinate</span><span class="sxs-lookup"><span data-stu-id="7c9f9-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="7c9f9-104">\[L'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è stato sostituito da [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7c9f9-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="7c9f9-105">Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="7c9f9-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="7c9f9-106">Se si connette un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a un controllo [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , toccare la penna del Tablet PC nella casella combinata modifica parte del controllo in fase di esecuzione, l'oggetto PenInputPanel non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="7c9f9-107">Tuttavia, viene visualizzato se si tocca la freccia a discesa.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="7c9f9-108">Ciò è dovuto al fatto che la finestra del controllo di modifica nella casella combinata non è la finestra che riceve i messaggi di penna.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="7c9f9-109">Le caselle combinate dispongono di una finestra di modifica figlio.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="7c9f9-110">La soluzione a questo problema consiste nel determinare se la finestra a cui è associato l'oggetto PenInputPanel presenta una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="7c9f9-111">In tal caso, è possibile alleghi l'oggetto PenInputPanel alla finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="7c9f9-112">Se si imposta la proprietà [VerticalOffset](/previous-versions/ms571983(v=vs.100)) dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) su un valore pari a-1, il pannello verrà visualizzato nella parte superiore della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7c9f9-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 
