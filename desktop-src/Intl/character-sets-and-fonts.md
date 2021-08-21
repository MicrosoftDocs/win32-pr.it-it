---
description: Windows consente la definizione locale di caratteri non standard sia nei set di caratteri a byte doppio (DBCS) che in Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Set di caratteri e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068281"
---
# <a name="character-sets-and-fonts"></a>Set di caratteri e tipi di carattere

Windows consente la definizione locale di caratteri [](double-byte-character-sets.md) non standard in set di caratteri a byte doppio (DBCS) e [Unicode.](unicode.md) Per un dbcs, questi caratteri non standard sono noti come caratteri definiti dall'utente finale (EUDC). Unicode offre una funzionalità simile tramite la relativa area di utilizzo privato (PUA). Le applicazioni identificano un carattere specificato utilizzando il valore del carattere DBCS o Unicode associato.

I valori dei caratteri DBCS che possono essere assegnati dipendono dal set di caratteri specificato. Ogni tabella codici [Windows'Asia](code-pages.md) orientale ha almeno un intervallo di valori riservati da usare come UDC. Gli intervalli sono definiti dalla chiave del Registro [di sistema EUDCCodeRange.](eudccoderange.md) I valori Unicode a questo scopo provengono sempre da PUA Unicode, dai valori da U+E000 a U+F8FF, da U+F0000 a U+FFFFD e da U+100000 a U+10FFFD.

Per creare un carattere EUDC o PUA, l'utente sceglie un valore di carattere compreso nell'intervallo specificato e aggiunge il [glifo](uniscribe-glossary.md) al tipo di carattere nella voce corrispondente al valore del carattere. L'utente crea il glifo usando un editor EUDC o un pacchetto di tipi di carattere acquistato da un fornitore di tipi di carattere. Qualsiasi tipo di carattere DBCS può contenere EUDC e qualsiasi tipo di carattere Unicode può contenere caratteri PUA. Il tipo di carattere è denominato tipo di carattere EUDC/PUA "separato" se contiene solo UDC. Il tipo di carattere è un tipo di carattere EUDC/PUA "integrato" se contiene caratteri standard e UDC.

Il tipo di carattere EUDC/PUA predefinito del sistema è un tipo di carattere che il sistema operativo associa automaticamente a tutti i tipi di carattere DBCS e Unicode, ad eccezione dei tipi di carattere a cui sono associati in modo esplicito i tipi di carattere EUDC/PUA. Le applicazioni impostano il tipo di carattere EUDC/PUA predefinito del sistema impostando il valore del nome SystemDefaultEUDCFont nella chiave del Registro [di sistema EUDC.](eudc.md) Analogamente, le applicazioni possono associare tipi di carattere EUDC/PUA separati ai tipi di carattere corrispondenti specificando un nome di carattere e il file del tipo di carattere associato sotto la chiave EUDC. Il sistema operativo tenta sempre prima di tutto di trovare EUDC/PUA nel tipo di carattere attualmente selezionato. Se il tipo di carattere non viene trovato, il sistema operativo cerca il carattere nel tipo di carattere EUDC/PUA associato, se ne è stato definito uno per il tipo di carattere attualmente selezionato. Se il carattere non viene trovato, il sistema operativo lo cerca nel tipo di carattere EUDC/PUA predefinito del sistema.

I tipi di carattere TrueType possono essere installati come file con estensione ttf o come file con estensione tte. Poiché il sistema operativo nasconde i file con estensione tte, le applicazioni non possono enumerare o esaminare in altro modo i tipi di carattere installati usando le funzioni dell'API GDI. In molti sistemi operativi il tipo di carattere EUDC/PUA predefinito del sistema e i tipi di carattere EUDC/PUA separati vengono installati come file con estensione tte. Per aggiungere, modificare ed eliminare tali tipi di carattere, le applicazioni come gli editor EUDC e Pannello di controllo devono utilizzare le voci del Registro di sistema.

L'uso di caratteri EUDC e PUA non mantiene in modo affidabile il significato in computer o set di caratteri diversi. Vedere [End-User-Defined and Private Use Area Characters](end-user-defined-characters.md) (Caratteri dell'area di utilizzo privato e definiti dall'utente finale) per altre informazioni sull'uso dei caratteri EUDC e PUA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caratteri dell'area di utilizzo privato e definiti dall'utente finale](end-user-defined-characters.md)
</dt> </dl>

 

 



