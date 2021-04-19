---
description: Anteporre sempre un prefisso a un file di testo normale Unicode con una byte order mark, che informa un'applicazione che riceve il file che il file è ordinato per byte.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Uso di byte order mark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319485"
---
# <a name="using-byte-order-marks"></a>Uso di byte order mark

Anteporre sempre un prefisso a un file di testo normale Unicode con una byte order mark, che informa un'applicazione che riceve il file che il file è ordinato per byte. I contrassegni per l'ordine dei byte disponibili sono elencati nella tabella seguente. Poiché il testo normale Unicode è una sequenza di valori di codice a 16 bit, è sensibile all'ordinamento dei byte utilizzato quando viene scritto il testo.

> [!Note]  
> Un byte order mark non è un carattere di controllo che consente di selezionare l'ordine dei byte del testo.

 



| Indicatore dell'ordine dei byte | Descrizione           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FE FF           | UTF-16, little endian |
| FF FE           | UTF-16, big endian    |
| FF FE 00 00     | UTF-32, little endian |
| 00 00 FE FF     | UTF-32, big-endian    |



 

> [!Note]  
> Microsoft usa l'ordine di byte UTF-16 little endian.

 

Idealmente, tutto il testo Unicode segue solo un set di regole di ordinamento dei byte. Questa operazione non è tuttavia possibile, perché i microprocessori differiscono dal posizionamento del byte meno significativo. I processori Intel e MIPS posizionano prima di tutto il byte meno significativo, mentre i processori Motorola (e tutti i file Unicode invertiti in byte) lo posizionano per ultimo. Con un solo set di regole di ordinamento dei byte, gli utenti di un microprocessore sono costretti a scambiare l'ordine dei byte ogni volta che viene letto o scritto un file di testo normale, anche se il file non viene mai trasferito a un altro sistema operativo in base a un microprocessore diverso.

La posizione preferita per specificare l'ordine dei byte è l'intestazione di un file, ma i file di testo non hanno intestazioni. Di conseguenza, Unicode ha definito un carattere (U + FEFF) e un carattere non carattere (U + FFFE) come Byte Order Mark. Sono immagini di byte mirror.

Poiché la sequenza U + FEFF è estremamente rara all'inizio di un normale file di testo non Unicode, può fungere da marcatore o firma implicita per identificare il file come file Unicode. Le applicazioni che leggono i file di testo sia Unicode che non Unicode devono usare la presenza di questa sequenza come indicatore del fatto che il file è probabilmente un file Unicode. Confrontare questa tecnica con l'uso del marcatore EOF di MS-DOS per terminare i file di testo.

Quando un'applicazione trova U + FEFF all'inizio di un file di testo, in genere elabora il file come file Unicode, anche se può eseguire ulteriori controlli euristici per la verifica. Un controllo di questo tipo può essere semplice come il test per verificare se la variazione nei byte di ordine inferiore è molto più alta rispetto alla variazione nei byte di ordine superiore. Se, ad esempio, il testo ASCII viene convertito in testo Unicode, ogni secondo byte è 0. Inoltre, il controllo per i caratteri di ritorno a capo e avanzamento riga (U + 000A e U + d) e per le dimensioni del file pari o dispari può fornire un indicatore forte della natura del file.

Quando un'applicazione trova U + FFFE all'inizio di un file di testo, lo interpreta per indicare che si tratta di un file Unicode invertito in byte. L'applicazione può scambiare l'ordine dei byte o avvisare l'utente che si è verificato un errore.

Poiché il carattere di byte order mark Unicode non viene trovato in alcuna tabella codici, scompare se i dati vengono convertiti in ANSI. A differenza di altri caratteri Unicode, non viene sostituito da un carattere predefinito quando viene convertito. Se un byte order mark viene trovato al centro di un file, non viene interpretato come carattere Unicode e non ha alcun effetto sull'output di testo.

> [!Note]  
> Il valore Unicode U + FFFF non è valido in file di testo normale e non può essere passato tra le applicazioni. È riservata per l'uso privato di un'applicazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



