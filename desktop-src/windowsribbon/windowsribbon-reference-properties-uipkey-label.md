---
title: UI_PKEY_Label
description: Identifica la proprietà \_ UI PKEY \_ Label.
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706432"
---
# <a name="ui_pkey_label"></a>Etichetta \_ PKEY \_ dell'interfaccia utente

Identifica la proprietà \_ UI PKEY \_ Label.

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

L'etichetta PKEY dell'interfaccia utente viene usata da un'applicazione per eseguire query sul testo dell'etichetta di \_ schede, gruppi, pulsanti, elementi della raccolta \_ e altri controlli della barra multifunzione.

> [!Note]  
> Windows 8 e più recente: [l'immagine del pulsante Del menu](windowsribbon-controls-applicationmenu.md) dell'applicazione è stata modificata in etichetta: **File**. È consigliabile non usare File come etichetta per le schede personalizzate.

 

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.

> [!Note]  
> Usare il riferimento ai caratteri XML del set di caratteri universali (UCS) `&#xA;` per specificare un'interruzione di riga.

 

L'allineamento a destra non è supportato.

La lunghezza massima dell'etichetta \_ PKEY \_ dell'interfaccia utente non è associata.

Se un comando viene esposto tramite una voce di menu e il valore di [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o UI PKEY Label contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata sia come descrizione comando che come tasto di scelta rapida per tale comando dal framework della barra \_ \_ multifunzione.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione di carattere speciale con una doppia e commerciale ( `&&` ) come illustrato nell'esempio seguente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà risorsa](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




