---
description: La stringa di composizione è il testo corrente nella finestra di composizione.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Stringa di composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cb63163ca9a8076edc4d01053e4baeffc619c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967627"
---
# <a name="composition-string"></a>Stringa di composizione

La stringa di composizione è il testo corrente nella finestra di composizione. Si tratta del testo che l'IME converte in caratteri finali. Ogni stringa di composizione è costituita da una o più clausole ". Una clausola è la più piccola combinazione di caratteri che l'IME può convertire in un carattere finale. Per ottenere e impostare la stringa di composizione, l'applicazione chiama rispettivamente le funzioni [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) .

Quando l'utente immette testo nella finestra di composizione, l'IME tiene traccia dello stato della stringa di composizione. Questo stato include informazioni sugli attributi, informazioni sulla clausola, informazioni di digitazione e posizione del cursore. L'applicazione può recuperare lo stato di composizione tramite la funzione [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) .

Viene eseguito il rendering delle informazioni sugli attributi in una matrice di valori a 8 bit che specifica lo stato dei caratteri nella stringa di composizione. Tutti i caratteri di una clausola devono avere lo stesso attributo. La matrice include un valore per ogni byte nella stringa, incluso un byte per il lead e il secondo byte di qualsiasi carattere a byte doppio nella stringa. Per ogni valore nella matrice, i bit da 0 a 3 possono essere una combinazione dei valori seguenti.



| Valore                      | Significato                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| \_input attr                | Carattere immesso dall'utente. L'IME deve ancora convertire questo carattere.                           |
| \_errore di input attr \_         | Carattere di errore che l'IME non è in grado di convertire. L'IME, ad esempio, non può riunire alcune consonanti. |
| \_destinazione attr \_ convertita    | Carattere selezionato dall'utente e quindi convertito dall'IME.                                             |
| ATTR \_ convertito            | Carattere già convertito nell'IME.                                                             |
| ATTR \_ destinazione \_ NOTCONVERTED | Carattere da convertire. L'utente ha selezionato questo carattere ma non è ancora stato convertito dall'IME.     |
| ATTR \_ FIXEDCONVERTED       | Caratteri che non saranno più convertiti dall'IME.                                                           |



 

Tutti gli altri valori sono riservati. In giapponese, qualsiasi carattere non convertito con l'attributo di \_ input attr è un carattere hiragana, Katakana o alfanumerico. In coreano questo attributo rappresenta un carattere hangul non ancora convertito nell'IME. In cinese tradizionale e cinese semplificato, ogni IME può limitare il proprio carattere all'interno di un intervallo.

Le informazioni sulla clausola incluse nello stato della stringa di composizione sono una matrice di valori a 32 bit che specifica le posizioni delle clausole nella stringa di composizione. La matrice include un valore per ogni clausola e un valore finale che specifica la lunghezza della stringa completa. Ogni valore nella matrice specifica l'offset, in byte, dall'inizio della stringa alla clausola. Il primo valore è sempre 0 perché la prima clausola inizia sempre dall'inizio della stringa. Se, ad esempio, in una stringa sono presenti due clausole, le informazioni sulla clausola hanno tre valori: il primo valore è 0, il secondo valore è l'offset della seconda clausola e il terzo valore corrisponde alla lunghezza della stringa. Per Unicode, la posizione di una clausola viene conteggiata in caratteri Unicode e la lunghezza di una stringa è la dimensione dei caratteri Unicode.

Le informazioni di tipizzazione incluse nello stato della stringa di composizione sono una stringa di caratteri con terminazione null che rappresenta i caratteri immessi dall'utente sulla tastiera.

La posizione del cursore inclusa nello stato della stringa di composizione è un valore che indica la posizione del cursore rispetto ai caratteri nella stringa di composizione. Il valore è l'offset, in byte, dall'inizio della stringa. Se questo valore è 0, il cursore si trova immediatamente prima del primo carattere nella stringa. Se il valore è uguale alla lunghezza della stringa, il cursore si trova immediatamente dopo l'ultimo carattere. Se il valore è 1, il cursore non è presente. Per Unicode, la posizione e la lunghezza sono misurate in caratteri Unicode.

L'applicazione può impostare la stringa di composizione o gli elementi dello stato di composizione utilizzando la funzione [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) . Per assicurarsi che la finestra di composizione aggiorni l'aspetto in base a queste modifiche, la funzione consente all'applicazione di inviare un messaggio di notifica alla finestra. Le applicazioni che impostano una combinazione di elementi di stato composizione in genere disabilitano le notifiche per tutte le chiamate, tranne l'ultima, in modo che venga generato un solo messaggio di notifica per la finestra di composizione.

Infine, il controllo di modifica supporta due messaggi per modificare la gestione delle stringhe di composizione dall'IME. Per altre informazioni, vedere [**em \_ GETIMESTATUS**](../controls/em-getimestatus.md) e [**em \_ SETIMESTATUS**](../controls/em-setimestatus.md). Per ulteriori informazioni sul controllo di modifica, vedere [modifica del controllo](../controls/edit-controls.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
