---
description: La proprietà ColorKey imposta o recupera la chiave di colore usata nei sottotitoli codificati.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Proprietà ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abca1dabbdb67f4380dbe32acbf2948862695b7c424dfd08629ec16237bb88c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073735"
---
# <a name="colorkey-property"></a>Proprietà ColorKey

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `ColorKey` proprietà imposta o recupera la chiave di colore utilizzata nei sottotitoli codificati.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il colore da utilizzare come sfondo trasparente per il testo con sottotitoli codificati. Il valore predefinito in 256 colori è magenta e off-black in qualsiasi altra profondità di colore.

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura. Questa proprietà si applica solo ai sottotitoli codificati, se presenti, non al flusso di immagini secondarie.

 

 



