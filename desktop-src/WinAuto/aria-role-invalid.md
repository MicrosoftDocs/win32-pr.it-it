---
title: Errore del ruolo ARIA
description: Errore del ruolo ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134014"
---
# <a name="aria-role-error"></a>Errore del ruolo ARIA

## <a name="text"></a>Testo

Il ruolo WAI-ARIA dell'elemento non è valido.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a tutti gli elementi con [**l'attributo role.**](https://developer.mozilla.org/docs/Web/HTML/Reference) Indica che l'attributo **role** non è un valore di ruolo WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) valido, come definito dalla specifica WAI-ARIA. L'impostazione di un ruolo valido garantisce che l'elemento venga interpretato correttamente dalle utilità per la lettura dello schermo e da assistive technology strumenti.

Per correggere l'errore, impostare [**l'attributo role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un valore di ruolo WAI-ARIA valido. Si noti che i ruoli WAI-ARIA astratti non sono validi.

## <a name="example"></a>Esempio


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore del ruolo contenitore ARIA](aria-container-role.md)
</dt> </dl>

 

 




