---
description: La proprietà TotalTitleTime recupera il tempo di riproduzione totale per il titolo corrente.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Proprietà TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650851"
---
# <a name="totaltitletime-property"></a>Proprietà TotalTitleTime

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `TotalTitleTime` proprietà recupera il tempo di riproduzione totale per il titolo corrente.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valore restituito

Restituisce il tempo di riproduzione totale del titolo corrente come stringa nel formato "hh:mm:ss:ff".

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. La stringa restituita avrà una lunghezza di 11 caratteri nel formato "hh:mm:ss:ff" (ore, minuti, secondi, fotogrammi).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



