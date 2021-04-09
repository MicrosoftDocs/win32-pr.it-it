---
title: UI_PKEY_Keytip
description: Identifica la proprietà del suggerimento dell'interfaccia utente \_ pkey \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955537"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="45087-103">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="45087-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="45087-104">Identifica la proprietà del suggerimento dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="45087-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="45087-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="45087-105">Remarks</span></span>

<span data-ttu-id="45087-106">L'interfaccia utente \_ \_ del suggerimento utente pkey viene utilizzata da un'applicazione per eseguire una query sull'acceleratore tastiera di un controllo Ribbon.</span><span class="sxs-lookup"><span data-stu-id="45087-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="45087-107">Il valore di questa proprietà è una stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="45087-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="45087-108">Il valore del \_ tasto di \_ scelta rapida UI pkey funge da tasto di scelta rapida per un comando, a meno che il comando non venga esposto tramite una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="45087-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="45087-109">In questo caso, il Framework ignora il valore del \_ suggerimento tasto di pkey dell'interfaccia utente \_ e usa invece un carattere preceduto da una e commerciale come specificato dall'etichetta [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="45087-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="45087-110">Se nessuna e commerciale è specificata da **Command. LabelTitle** o dall'etichetta pkey dell'interfaccia utente \_ \_ , non viene esposto alcun tasto di scelta rapida o tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="45087-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="45087-111">La lunghezza massima del suggerimento tasto di pkey dell'interfaccia utente \_ \_ è unbounded.</span><span class="sxs-lookup"><span data-stu-id="45087-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45087-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45087-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45087-113">Proprietà delle risorse</span><span class="sxs-lookup"><span data-stu-id="45087-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="45087-114">**Command. suggerimento**</span><span class="sxs-lookup"><span data-stu-id="45087-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




