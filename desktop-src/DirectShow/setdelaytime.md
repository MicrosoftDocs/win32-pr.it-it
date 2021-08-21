---
description: Il metodo SetDelayTime imposta il tempo di ritardo per la descrizione comando associata all'oggetto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ebd119f20977c98aa2664518dc2125b7b5c157b44ff53c3a37740bf40a1677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683741"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetDelayTime` metodo imposta il tempo di ritardo per la descrizione comando associata all'oggetto **MSWebDVD.**

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Specifica il tipo di ritardo come integer.



| Valore | Descrizione                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Per reimpostare il tempo di ritardo del popolamento automatico sul valore predefinito, impostare *iNewVal* su -1.                                                                                                                                                                       |
| 0     | Impostare il periodo di tempo per cui una finestra della descrizione comando rimane visibile se il puntatore è posizionato all'interno del rettangolo di delimitazione di uno strumento.                                                                                                                         |
| 1     | Impostare il periodo di tempo per cui un puntatore deve rimanere stazionare all'interno del rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.                                                                                                                    |
| 2     | Impostare il tempo necessario per visualizzare le finestre della descrizione comando successive quando il puntatore si sposta da uno strumento a un altro.                                                                                                                          |
| 3     | Impostare tutti i tempi di ritardo su proporzioni predefinite. Il tempo di ripopolamento automatico è dieci volte l'ora iniziale e il tempo di sincronizzazione è un quinto l'ora iniziale. Se questo flag è impostato, usare un valore positivo di iNewVal per specificare l'ora iniziale, in millisecondi. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Specifica il ritardo, in millisecondi, come integer.



| Valore                    | Descrizione                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Imposta il ritardo specificato in *iDelayType* sul valore predefinito |
| qualsiasi altro valore negativo | Imposta tutti i tipi di ritardo sul valore predefinito.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

 

 



