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
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Uso di PenInputPanel con caselle combinate

\[L'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è stato sostituito da [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]

Se si connette un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a un controllo [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , toccare la penna del Tablet PC nella casella combinata modifica parte del controllo in fase di esecuzione, l'oggetto PenInputPanel non viene visualizzato. Tuttavia, viene visualizzato se si tocca la freccia a discesa. Ciò è dovuto al fatto che la finestra del controllo di modifica nella casella combinata non è la finestra che riceve i messaggi di penna. Le caselle combinate dispongono di una finestra di modifica figlio. La soluzione a questo problema consiste nel determinare se la finestra a cui è associato l'oggetto PenInputPanel presenta una finestra figlio. In tal caso, è possibile alleghi l'oggetto PenInputPanel alla finestra figlio.

Se si imposta la proprietà [VerticalOffset](/previous-versions/ms571983(v=vs.100)) dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) su un valore pari a-1, il pannello verrà visualizzato nella parte superiore della casella combinata.

 

 
