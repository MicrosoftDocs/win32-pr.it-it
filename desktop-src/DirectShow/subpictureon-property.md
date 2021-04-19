---
description: La proprietà SubpictureOn imposta o recupera lo stato della sottoimmagine corrente (on o off).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Proprietà SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317836"
---
# <a name="subpictureon-property"></a>Proprietà SubpictureOn

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `SubpictureOn` proprietà imposta o recupera lo stato della sottoimmagine corrente (on o off).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se viene visualizzata la sottoimmagine.

## <a name="remarks"></a>Commenti

Questa proprietà non ha effetto sulla visualizzazione di didascalie chiuse. I sottotitoli sono incorporati nel flusso video. Le sottoimmagini DVD vengono trasferite in un flusso separato.

Quando il flusso di sottoimmagine viene modificato utilizzando [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` proprietà passa a **true**.

Questa proprietà è di lettura/scrittura e il valore predefinito è false.

 

 



