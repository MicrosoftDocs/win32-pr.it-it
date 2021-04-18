---
description: Windows consente la definizione locale di caratteri non standard sia nei set di caratteri a doppio byte (DBCS) che in Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Set di caratteri e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbf3dae2875ec6d714419bb45411f3208bfe5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306613"
---
# <a name="character-sets-and-fonts"></a>Set di caratteri e tipi di carattere

Windows consente la definizione locale di caratteri non standard sia nei [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) che in [Unicode](unicode.md). Per un DBCS, questi caratteri non standard sono noti come caratteri definiti dall'utente finale (EUDC). Unicode fornisce una funzionalità simile tramite l'area di utilizzo privato (PUA). Le applicazioni identificano un carattere specificato utilizzando il valore DBCS o il carattere Unicode associato.

I valori dei caratteri DBCS che possono essere assegnati dipendono dal set di caratteri specificato. Ogni [tabella codici](code-pages.md) di Windows Asia orientale presenta almeno un intervallo di valori riservati da usare come EUDCs. Gli intervalli sono definiti dalla chiave del registro di sistema [EUDCCodeRange](eudccoderange.md) . I valori Unicode per questo scopo derivano sempre da Unicode PUA, i valori U + E000 a U + F8FF, U + F0000 a U + FFFFD e U + 100000 a U + 10FFFD.

Per creare un carattere EUDC o PUA, l'utente sceglie un valore di carattere compreso nell'intervallo specificato e aggiunge il [glifo](uniscribe-glossary.md) al tipo di carattere nella voce corrispondente a tale valore. L'utente crea il glifo usando un editor EUDC o un pacchetto di tipi di carattere acquistato da un fornitore di tipi di carattere. Tutti i tipi di carattere DBCS possono contenere EUDCs e qualsiasi tipo di carattere Unicode può contenere caratteri PUA. Il tipo di carattere è denominato "separato" EUDC/PUA se contiene solo EUDCs. Il tipo di carattere è "Integrated" EUDC/PUA se contiene caratteri standard e EUDCs.

Il tipo di carattere EUDC/PUA predefinito del sistema è un tipo di carattere che il sistema operativo associa automaticamente a tutti i tipi di carattere DBCS e Unicode, ad eccezione dei tipi di carattere a cui sono stati associati in modo esplicito i tipi Le applicazioni impostano il tipo di carattere EUDC/PUA predefinito del sistema impostando il valore del nome SystemDefaultEUDCFont nella chiave del registro di sistema [EUDC](eudc.md) . Analogamente, le applicazioni possono associare tipi di carattere EUDC/PUA separati con i tipi di carattere corrispondenti specificando un nome di tipo di carattere e il file del tipo di carattere associato nella chiave Il sistema operativo tenta sempre di trovare il EUDC/PUA nel tipo di carattere attualmente selezionato. Se il tipo di carattere non viene trovato, il sistema operativo cerca il carattere nel tipo di carattere EUDC/PUA associato, se ne è stato definito uno per il tipo di carattere correntemente selezionato. Se il carattere non è ancora in grado di trovare il carattere, il sistema operativo lo cerca nel tipo di carattere predefinito di sistema EUDC/PUA.

I tipi di carattere TrueType possono essere installati come file. ttf o come file con estensione TTE. Poiché il sistema operativo nasconde i file con estensione TTE, le applicazioni non possono enumerare o altrimenti esaminare i tipi di carattere installati utilizzando le funzioni dell'API GDI. In molti sistemi operativi, il tipo di carattere predefinito di sistema EUDC/PUA e i tipi di carattere separati EUDC/PUA vengono installati come file con estensione TTE. Le applicazioni, ad esempio gli editor EUDC e il pannello di controllo, devono usare le voci del registro di sistema per aggiungere, modificare ed eliminare tali tipi di carattere.

L'uso di caratteri EUDC e PUA non mantiene in modo affidabile il significato in diversi computer o set di caratteri. Per ulteriori attenzioni sull'utilizzo di caratteri EUDC e PUA, vedere [caratteri di area di utilizzo privato e definiti dall'utente finale](end-user-defined-characters.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caratteri dell'area uso privato e definiti dall'utente finale](end-user-defined-characters.md)
</dt> </dl>

 

 



