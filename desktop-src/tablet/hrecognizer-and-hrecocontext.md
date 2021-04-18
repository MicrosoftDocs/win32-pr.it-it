---
description: Si fa riferimento a un riconoscitore Ink con un handle HRECOGNIZER e un contesto di riconoscimento come handle HRECOCONTEXT. Una libreria di collegamento dinamico (DLL) di riconoscimento può implementare i riconoscitori per più di un linguaggio.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER e HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307481"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER e HRECOCONTEXT

Si fa riferimento a un riconoscitore Ink con un handle [HRECOGNIZER](hrecognizer-handle.md) e un contesto di riconoscimento come handle [HRECOCONTEXT](hrecocontext-handle.md) .

Una libreria di collegamento dinamico (DLL) di riconoscimento può implementare i riconoscitori per più di un linguaggio. In tal caso, ogni lingua viene selezionata da un CLSID passato durante la creazione dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) nell'applicazione. Inoltre, una DLL del riconoscitore può creare più handle di riconoscimento quando viene caricato, uno o più per ogni lingua riconosciuta.

Viene creato un contesto di riconoscimento per rappresentare l'evento di riconoscimento di uno specifico input penna. Quando viene creato il contesto, l'handle degli oggetti riconoscimento associato viene passato alla funzione [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) . In questo caso il linguaggio viene associato al contesto del riconoscimento.

Un contesto di riconoscimento può rappresentare il riconoscimento di tutto l'input penna nel corpo di un messaggio di posta elettronica, l'input penna di un singolo campo all'interno di un'applicazione o una singola riga di testo scritta nel pannello di input di Tablet PC. Il volume di input penna in un singolo contesto di riconoscimento può variare da un singolo tratto a una pagina intera o più.

Il contesto del riconoscimento è definito dalle impostazioni di:

-   Guida al riconoscimento.
-   Qualsiasi factoids.
-   Qualsiasi flag.
-   Contesto del testo.
-   Qualsiasi elenco di parole.
-   Modalità di completamento automatico dei caratteri.

L'handle per il contesto di riconoscimento viene passato a tutte le funzioni che utilizzano queste impostazioni. Se si modifica un'impostazione, il contesto di riconoscimento viene modificato.

L'applicazione può usare diversi contesti per riconoscere l'input penna da diverse parti dello schermo. Un singolo contesto può riconoscere più righe di testo. Tuttavia, un singolo contesto non può elaborare due paragrafi scritti side-by-Side, ad esempio più colonne in un articolo di giornale.

Per riconoscere il nuovo input penna, creare un nuovo contesto. In alternativa, usare la funzione [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) per creare una copia di un contesto che non ha l'input penna e i risultati oppure la funzione [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) per cancellare un contesto dell'input penna e dei risultati. Con questi approcci, un'applicazione Ink può riutilizzare un contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzione seguide**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**Getguide (funzione)**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**SetFactoid (funzione)**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**Funzione seflags**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**SetEnabledUnicodeRanges (funzione)**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges (funzione)**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**SetCACMode (funzione)**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**SetTextContext (funzione)**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**Funzione WordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



