---
description: Il metodo ShowMenu visualizza il menu specificato sullo schermo.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Metodo ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb9135e2999675dc46774f15ee79afd835085b40fe210d0ca1cfd173f8a99fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050511"
---
# <a name="showmenu-method"></a>Metodo ShowMenu

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `ShowMenu` metodo visualizza il menu specificato sullo schermo.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Specifica l'ID menu come integer.



| Valore | Descrizione |
|-------|-------------|
| 2     | Titolo (in alto) |
| 3     | Radice        |
| 4     | Immagine secondaria  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Capitolo     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

I nomi dei menu DVD possono generare confusione. Il menu del titolo è un altro nome per il menu di Gestione video, il menu principale per l'intero disco; in genere elenca tutti i set di titoli video disponibili sul disco. Il menu radice è il menu per un set di titoli video, che può contenere un titolo o un gruppo di titoli. Tutti i titoli di un set di titoli condividono gli stessi menu Immagine secondaria, Audio e Angolo.

 

 



