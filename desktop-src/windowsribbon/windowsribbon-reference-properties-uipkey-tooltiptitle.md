---
title: UI_PKEY_TooltipTitle
description: Identifica la proprietà \_ \_ TooltipTitle PKEY dell'interfaccia utente.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437786"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ TooltipTitle

Identifica la proprietà \_ \_ TooltipTitle PKEY dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

Ui PKEY TooltipTitle viene usato da un'applicazione per eseguire query sulla descrizione comando di \_ schede, gruppi, pulsanti, elementi della raccolta \_ e altri controlli della barra multifunzione.

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.

> [!Note]  
> Usare il riferimento ai caratteri XML del set di caratteri universali (UCS) `&#xA;` per specificare un'interruzione di riga.

 

L'allineamento a destra non è supportato.

La lunghezza massima di UI \_ PKEY \_ TooltipTitle non è associata.

Per visualizzare una e commerciale in una descrizione comando, eseguire l'escape della designazione di carattere speciale con una doppia e commerciale ( `&&` ) come illustrato nell'esempio seguente.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà risorsa](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




