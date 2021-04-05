---
description: La proprietà TotalTitleTime Recupera il tempo di riproduzione totale per il titolo corrente.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Proprietà TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882433"
---
# <a name="totaltitletime-property"></a>Proprietà TotalTitleTime

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `TotalTitleTime` proprietà recupera il tempo di riproduzione totale per il titolo corrente.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valore restituito

Restituisce il tempo di riproduzione totale del titolo corrente sotto forma di stringa nel formato "HH: mm: SS: FF".

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. La stringa restituita avrà una lunghezza di 11 caratteri nel formato "HH: mm: SS: FF" (hours, minutes, seconds, frames).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



