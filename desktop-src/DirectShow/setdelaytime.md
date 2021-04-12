---
description: Il metodo SetDelayTime imposta il tempo di ritardo per la descrizione comando associata all'oggetto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480588"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetDelayTime` metodo imposta il tempo di ritardo per la descrizione comando associata all'oggetto **mswebdvd** .

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Specifica il tipo di ritardo come intero.



| Valore | Descrizione                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Per reimpostare il valore predefinito di autopop delay, impostare *iNewVal* su-1.                                                                                                                                                                       |
| 0     | Imposta il periodo di tempo in cui una finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.                                                                                                                         |
| 1     | Imposta il periodo di tempo in cui un puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.                                                                                                                    |
| 2     | Consente di impostare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore viene spostato da uno strumento all'altro.                                                                                                                          |
| 3     | Imposta tutti i tempi di ritardo sulle proporzioni predefinite. Il tempo di autopop è dieci volte l'ora iniziale e il tempo di ripresentazione è pari a un quinto del tempo iniziale. Se questo flag è impostato, utilizzare un valore positivo di iNewVal per specificare il tempo iniziale, in millisecondi. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Specifica il ritardo, in millisecondi, come intero.



| Valore                    | Descrizione                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Imposta il valore predefinito del ritardo specificato in *iDelayType* |
| qualsiasi altro valore negativo | Imposta tutti i tipi di ritardo sul valore predefinito.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

 

 



