---
description: Descrive l'uso dell'oggetto PenInputPanel con caselle combinate.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Uso di PenInputPanel con caselle combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1e90d581e08f9a23346bbf13cf8c3866f6e947f1d9b23375248f3ba9c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589301"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Uso di PenInputPanel con caselle combinate

\[[L'oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è stato sostituito da [Microsoft.Ink.TextInput.](/previous-versions/ms581554(v=vs.100)) Fare riferimento a Programmazione [del pannello input di testo.](programming-the-text-input-panel.md)\]

Se associa un [oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a un controllo [ComboBox,](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) quindi tocca la penna del tablet nella casella combinata della parte del controllo di modifica in fase di esecuzione, l'oggetto PenInputPanel non viene visualizzato. Tuttavia, viene visualizzato se si tocca la freccia a discesa. Ciò è dovuto al fatto che la finestra del controllo di modifica nella casella combinata non è la finestra che riceve messaggi penna. Le caselle combinate hanno una finestra di modifica figlio. La soluzione a questo problema consiste nel determinare se la finestra a cui è collegato l'oggetto PenInputPanel ha una finestra figlio. In questo caso, puoi collegare l'oggetto PenInputPanel alla finestra figlio.

Impostando la [proprietà VerticalOffset](/previous-versions/ms571983(v=vs.100)) dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) su un valore pari a -1, il pannello viene visualizzato sopra la casella combinata.

 

 
