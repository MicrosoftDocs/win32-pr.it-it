---
description: La proprietà FullScreenMode imposta o recupera un valore che indica se la visualizzazione è in modalità schermo intero.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Proprietà FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015619"
---
# <a name="fullscreenmode-property"></a>Proprietà FullScreenMode

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `FullScreenMode` proprietà imposta o recupera un valore che indica se la visualizzazione è in modalità schermo intero.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se abilitare o disabilitare la riproduzione a schermo intero.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito false.



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| true  | Abilitare la riproduzione a schermo intero. Si tratta del valore predefinito. |
| false | Disabilitare la riproduzione a schermo intero.                          |



 

La modalità schermo intero è disponibile solo quando il controllo MSWebDVD è in esecuzione in modalità finestra.

 

 



