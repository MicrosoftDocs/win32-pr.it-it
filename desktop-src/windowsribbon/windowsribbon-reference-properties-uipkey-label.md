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
# <a name="ui_pkey_label"></a><span data-ttu-id="6015b-103">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="6015b-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="6015b-104">Identifica la \_ proprietà dell'etichetta pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="6015b-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="6015b-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="6015b-105">Remarks</span></span>

<span data-ttu-id="6015b-106">L' \_ etichetta pkey dell'interfaccia utente \_ viene usata da un'applicazione per eseguire una query sul testo dell'etichetta di schede, gruppi, pulsanti, elementi della raccolta e altri controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6015b-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="6015b-107">Windows 8 e versioni successive: l'immagine del pulsante di [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) è cambiata in etichetta: **file**.</span><span class="sxs-lookup"><span data-stu-id="6015b-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="6015b-108">Si consiglia di non usare file come etichetta per le schede.</span><span class="sxs-lookup"><span data-stu-id="6015b-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="6015b-109">Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="6015b-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="6015b-110">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="6015b-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="6015b-111">L'allineamento a destra non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6015b-111">Right alignment is not supported.</span></span>

<span data-ttu-id="6015b-112">La lunghezza massima dell'etichetta pkey dell'interfaccia utente non \_ \_ è associata.</span><span class="sxs-lookup"><span data-stu-id="6015b-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="6015b-113">Se un comando viene esposto tramite una voce di menu e il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o dell'etichetta pkey dell'interfaccia utente \_ \_ contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata come un tasto di scelta rapida e un tasto di scelta rapida per tale comando dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6015b-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="6015b-114">Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="6015b-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="6015b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6015b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6015b-116">Proprietà delle risorse</span><span class="sxs-lookup"><span data-stu-id="6015b-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="6015b-117">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="6015b-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="6015b-118">Interfaccia utente \_ pkey \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="6015b-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




