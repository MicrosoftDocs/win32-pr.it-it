---
title: UI_PKEY_Label
description: Identifica la \_ proprietà dell'etichetta pkey dell'interfaccia utente \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856417"
---
# <a name="ui_pkey_label"></a>\_Etichetta pkey dell'interfaccia utente \_

Identifica la \_ proprietà dell'etichetta pkey dell'interfaccia utente \_ .

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

L' \_ etichetta pkey dell'interfaccia utente \_ viene usata da un'applicazione per eseguire una query sul testo dell'etichetta di schede, gruppi, pulsanti, elementi della raccolta e altri controlli della barra multifunzione.

> [!Note]  
> Windows 8 e versioni successive: l'immagine del pulsante di [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) è cambiata in etichetta: **file**. Si consiglia di non usare file come etichetta per le schede.

 

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

L'allineamento a destra non è supportato.

La lunghezza massima dell'etichetta pkey dell'interfaccia utente non \_ \_ è associata.

Se un comando viene esposto tramite una voce di menu e il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o dell'etichetta pkey dell'interfaccia utente \_ \_ contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata come un tasto di scelta rapida e un tasto di scelta rapida per tale comando dal framework della barra multifunzione.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà delle risorse](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




