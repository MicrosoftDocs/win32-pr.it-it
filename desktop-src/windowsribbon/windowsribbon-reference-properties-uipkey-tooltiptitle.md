---
title: UI_PKEY_TooltipTitle
description: Identifica la proprietà TooltipTitle dell'interfaccia utente \_ pkey \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298605"
---
# <a name="ui_pkey_tooltiptitle"></a>Interfaccia utente \_ pkey \_ TooltipTitle

Identifica la proprietà TooltipTitle dell'interfaccia utente \_ pkey \_ .

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

L'interfaccia utente \_ pkey \_ TooltipTitle viene utilizzata da un'applicazione per eseguire una query sulla descrizione comando di schede, gruppi, pulsanti, elementi della raccolta e altri controlli della barra multifunzione.

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

L'allineamento a destra non è supportato.

La lunghezza massima dell'interfaccia utente \_ pkey \_ TooltipTitle è unbounded.

Per visualizzare una e commerciale in una descrizione comando, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà delle risorse](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




