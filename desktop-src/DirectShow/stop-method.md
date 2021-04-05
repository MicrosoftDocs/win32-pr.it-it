---
description: Il metodo Stop interrompe la riproduzione.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Metodo Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968148"
---
# <a name="stop-method-directshow"></a>Metodo Stop (DirectShow)

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Stop` metodo interrompe la riproduzione.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se [**EnableResetOnStop**](enableresetonstop-property.md) è impostato su true, la chiamata a `Stop` inserisce lo strumento di navigazione del DVD, insieme al resto del grafico del filtro, nello stato interrotto, il che significa che alla successiva pressione del pulsante **Play** la riproduzione inizia all'inizio del disco. Se **EnableResetOnStop** è impostato su true, la riproduzione riprende dal punto in cui si è interrotta quando l'utente rilascia il comando di **riproduzione** successivo.

 

 



