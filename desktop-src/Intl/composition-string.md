---
description: La stringa di composizione è il testo corrente nella finestra di composizione.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Stringa di composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a547b4383c95b99025b779de2950c8325af56a3397603db10199474dfe20ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430991"
---
# <a name="composition-string"></a>Stringa di composizione

La stringa di composizione è il testo corrente nella finestra di composizione. Si tratta del testo convertito dall'IME in caratteri finali. Ogni stringa di composizione è costituita da una o più "clausole". Una clausola è la combinazione più piccola di caratteri che l'IME può convertire in un carattere finale. Per ottenere e impostare la stringa di composizione, l'applicazione chiama rispettivamente le funzioni [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e [**ImmSetCompositionString.**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)

Quando l'utente immette testo nella finestra di composizione, l'IME tiene traccia dello stato della stringa di composizione. Questo stato include le informazioni sugli attributi, le informazioni sulla clausola, le informazioni di digitazione e la posizione del cursore. L'applicazione può recuperare lo stato della composizione usando la [**funzione ImmGetCompositionString.**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)

Il rendering delle informazioni sugli attributi viene eseguito in una matrice di valori a 8 bit che specifica lo stato dei caratteri nella stringa di composizione. Tutti i caratteri di una clausola devono avere lo stesso attributo. La matrice include un valore per ogni byte nella stringa, incluso un byte ciascuno per il byte iniziale e il secondo byte di qualsiasi carattere a byte doppio nella stringa. Per ogni valore della matrice, i bit da 0 a 3 possono essere una combinazione dei valori seguenti.



| Valore                      | Significato                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| ATTR \_ INPUT                | Carattere immesso dall'utente. L'IME deve ancora convertire questo carattere.                           |
| ERRORE \_ DI INPUT \_ ATTR         | Carattere di errore che l'IME non può convertire. Ad esempio, l'IME non può mettere insieme alcune consonanti. |
| DESTINAZIONE ATTR \_ \_ CONVERTITA    | Carattere selezionato dall'utente e quindi convertito dall'IME.                                             |
| ATTR \_ CONVERTITO            | Carattere già convertito dall'IME.                                                             |
| DESTINAZIONE ATTR \_ \_ NOTCONVERTED | Carattere da convertire. L'utente ha selezionato questo carattere, ma l'IME non lo ha ancora convertito.     |
| ATTR \_ FIXEDCONVERTED       | Caratteri che l'IME non convertirà più.                                                           |



 

Tutti gli altri valori sono riservati. In giapponese, qualsiasi carattere non convertito con l'attributo ATTR INPUT è \_ un carattere hiragana, katakana o alfanumerico. In coreano, questo attributo rappresenta un carattere Hangul che l'IME non ha ancora convertito. In cinese tradizionale e cinese semplificato, ogni IME può limitarne il carattere all'interno di un intervallo.

Le informazioni sulla clausola incluse nello stato della stringa di composizione sono una matrice di valori a 32 bit che specifica le posizioni delle clausole nella stringa di composizione. La matrice include un valore per ogni clausola e un valore finale che specifica la lunghezza della stringa completa. Ogni valore nella matrice specifica l'offset, in byte, dall'inizio della stringa alla clausola . Il primo valore è sempre 0 perché la prima clausola inizia sempre all'inizio della stringa. Ad esempio, se una stringa ha due clausole, le informazioni sulla clausola hanno tre valori: il primo valore è 0, il secondo valore è l'offset della seconda clausola e il terzo valore è la lunghezza della stringa. Per Unicode, la posizione di una clausola viene conteggiata in caratteri Unicode e la lunghezza di una stringa è la dimensione in caratteri Unicode.

Le informazioni di digitazione incluse nello stato della stringa di composizione sono una stringa di caratteri con terminazione Null che rappresenta i caratteri immessi dall'utente sulla tastiera.

La posizione del cursore inclusa nello stato della stringa di composizione è un valore che indica la posizione del cursore rispetto ai caratteri nella stringa di composizione. Il valore è l'offset, in byte, dall'inizio della stringa. Se questo valore è 0, il cursore si trova immediatamente prima del primo carattere nella stringa. Se il valore è uguale alla lunghezza della stringa, il cursore si trova immediatamente dopo l'ultimo carattere. Se il valore è 1, il cursore non è presente. Per Unicode, sia la posizione che la lunghezza vengono misurate in caratteri Unicode.

L'applicazione può impostare la stringa di composizione o gli elementi dello stato della composizione usando la [**funzione ImmSetCompositionString.**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) Per assicurarsi che la finestra di composizione apportare modifiche, la funzione consente all'applicazione di inviare un messaggio di notifica alla finestra. Le applicazioni che impostano una combinazione di elementi di stato della composizione disabilitano in genere le notifiche per tutti gli elementi, ad eccezione dell'ultima chiamata a questa funzione, in modo che per la finestra di composizione sia generato un solo messaggio di notifica.

Infine, il controllo di modifica supporta due messaggi per la modifica della gestione delle stringhe di composizione da parte dell'IME. Per altre informazioni, vedere [**EM \_ GETIMESTATUS**](../controls/em-getimestatus.md) ed [**EM \_ SETIMESTATUS**](../controls/em-setimestatus.md). Per altre informazioni sul controllo di modifica, vedere [Modifica del controllo](../controls/edit-controls.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
