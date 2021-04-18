---
title: Errore del ruolo ARIA
description: Errore del ruolo ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300631"
---
# <a name="aria-role-error"></a>Errore del ruolo ARIA

## <a name="text"></a>Testo

L'elemento ha un ruolo WAI-ARIA non valido.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a tutti gli elementi che hanno l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) . Indica che l'attributo **Role** non è un valore di ruolo di Web Accessibility Initiative (Wai-aria) accessibile per Internet, come definito dalla specifica Wai-aria. L'impostazione di un ruolo valido consente di garantire che l'elemento venga interpretato correttamente dalle utilità per la lettura dello schermo e da altri strumenti di Assistive Technology.

Per correggere l'errore, impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un valore del ruolo Wai-aria valido. Si noti che i ruoli di WAI-ARIA astratti non sono validi.

## <a name="example"></a>Esempio


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore del ruolo del contenitore ARIA](aria-container-role.md)
</dt> </dl>

 

 




