---
description: Il metodo ShowMenu Visualizza il menu specificato sullo schermo.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Metodo ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746786"
---
# <a name="showmenu-method"></a>Metodo ShowMenu

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `ShowMenu` Metodo Visualizza il menu specificato sullo schermo.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Specifica l'ID del menu come intero.



| Valore | Descrizione |
|-------|-------------|
| 2     | Titolo (inizio) |
| 3     | Radice        |
| 4     | Sottoimmagine  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Capitolo     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

I nomi dei menu DVD possono avere un po' di confusione. Il menu titolo è un altro nome per il menu di gestione video, il menu principale per l'intero disco; Elenca in genere tutti i set di titoli video disponibili sul disco. Il menu radice è il menu per un set di titoli video, che può contenere un titolo o un gruppo di titoli. Tutti i titoli di un set di titoli condividono lo stesso menu di immagine, audio e angolo.

 

 



