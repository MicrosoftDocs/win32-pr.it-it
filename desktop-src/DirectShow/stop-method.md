---
description: Il metodo Stop arresta la riproduzione.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Metodo Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050111"
---
# <a name="stop-method-directshow"></a>Metodo Stop (DirectShow)

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Stop` metodo arresta la riproduzione.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se [**EnableResetOnStop**](enableresetonstop-property.md) è impostato su true, la chiamata di imposta lo strumento di spostamento dvd, insieme al resto del grafico dei filtri, in uno stato di arresto, il che significa che la volta successiva che l'utente preme il pulsante Riproduci, la riproduzione inizia all'inizio del `Stop` disco.  Se **EnableResetOnStop** è impostato su true, la riproduzione riprende dal punto in cui è stata ancorata quando l'utente esegue il comando **Play** successivo.

 

 



