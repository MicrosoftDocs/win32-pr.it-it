---
title: Errore di ARIA TabIndex
description: Errore di ARIA TabIndex
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047533"
---
# <a name="aria-tabindex-error"></a>Errore di ARIA TabIndex

## <a name="text"></a>Testo

L'elemento non è disabilitato e ha un gestore dell'evento **Click** , ma contiene **TabIndex** < 0 e non è nell'ordine di tabulazione per impostazione predefinita.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi che dispongono di un gestore dell'evento click e che non sono disabilitati. Questi elementi devono essere nell'ordine di tabulazione. In questo modo si garantisce che un elemento possa essere raggiunto usando il tasto TAB, che è il modo in cui gli utenti dello screen reader navigano in genere nell'interfaccia utente.

Per correggere l'errore, impostare l'attributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) su un valore uguale o maggiore di 0. Non è necessario impostare in modo esplicito l' **attributo tabIndex** per i tag presenti nell'ordine di tabulazione per impostazione predefinita, ad esempio un (con attributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), un [**pulsante**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (escluso "hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)e [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (come parte della mappa immagine).

## <a name="example"></a>Esempio


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




