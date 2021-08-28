---
description: Le applicazioni scrivono caratteri definiti dall'utente finale (EUDC) e caratteri dell'area di utilizzo privato (PUA) sullo schermo o sulla stampante esattamente come scrivono altri caratteri, usando funzioni di output come TextOut ed ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Scrittura, mapping e ordinamento di caratteri EUDC e PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ab43eb54055b97fe1823ad99467a4cd0b12a0a5fb971d52d225631cfd37ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102081"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Scrittura, mapping e ordinamento di caratteri EUDC e PUA

Le applicazioni scrivono caratteri definiti dall'utente finale (EUDC) e caratteri dell'area di utilizzo privato (PUA) sullo schermo o sulla stampante esattamente come scrivono altri caratteri, usando funzioni di output come [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) ed [ExtTextOut.](/windows/win32/api/wingdi/nf-wingdi-exttextouta) Queste funzioni recuperano automaticamente le informazioni sui caratteri dai tipi di carattere EUDC o PUA se EUDC è abilitato. Per altre informazioni, vedere [End-User \_ Defined and Private Use Area Characters](end-user-defined-characters.md).

Quando si scrivono caratteri EUDC o PUA, il funzionamento della funzione di output del testo dipende dal tipo di carattere attualmente selezionato. Se il tipo di carattere selezionato è un tipo di carattere EUDC o PUA integrato, la funzione recupera le informazioni sui caratteri da tale tipo di carattere. Se il tipo di carattere selezionato è un tipo di carattere TrueType del [set](double-byte-character-sets.md) di caratteri a byte doppio (DBCS) a cui è associato un tipo di carattere EUDC separato, la funzione recupera le informazioni dal tipo di carattere EUDC specificato. Analogamente, se il tipo di carattere selezionato è un tipo di carattere [TrueType Unicode](unicode.md) a cui è associato un tipo di carattere PUA separato, la funzione recupera le informazioni dal tipo di carattere PUA. Se al tipo di carattere selezionato non è associato un tipo di carattere EUDC o PUA, la funzione recupera le informazioni dal tipo di carattere EUDC predefinito del sistema. Se il carattere non è nel tipo di carattere EUDC predefinito del sistema o non è presente alcun tipo di carattere EUDC predefinito di sistema, la funzione scrive il carattere predefinito definito dal tipo di carattere selezionato.

Le applicazioni possono eseguire il mapping di EUDC da e verso Unicode usando le [**funzioni MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte.**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) La **funzione MultiByteToWideChar esegue** il mapping della maggior parte delle funzioni EUDC ai caratteri nella puA Unicode. Tuttavia, per supportare determinati standard nazionali o regionali, è possibile eseguire il mapping di alcuni EUDC a punti di codice Unicode non PUA. La funzione **WideCharToMultiByte** esegue il mapping di un carattere nella PUA alla controparte EUDC, se esiste un mapping di questo tipo e se il punto di codice non dispone di un mapping non PUA valido in Unicode. Non tutte le code pages hanno un intervallo EUDC. La tabella codici specificata in una chiamata a **WideCharToMultiByte** deve contenere un intervallo di codice EUDC per il mapping all'intervallo EUDC. Se la tabella codici non contiene un intervallo di codice EUDC, la funzione recupera il carattere predefinito per tutti i caratteri nella tabella codici Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) non garantiscono il mapping di round trip. In altre parole, è possibile iniziare con una particolare stringa multibyte contenente EUDC, eseguire il mapping della stringa a Unicode con **MultiByteToWideChar** ed eseguire il mapping al DBCS originale **con WideCharToMultiByte** e terminare con un risultato non identico alla stringa originale. Le applicazioni basate sul mapping EUDC a Unicode devono garantire che tutti i caratteri necessari possano eseguire il round trip tra l'area EUDC della tabella codici appropriata e l'area PUA Unicode.

Le applicazioni non devono tentare di eseguire il mapping di EUDC da una tabella codici a un'altra. Se un'applicazione inizia con un EUDC da una tabella codici, la esegue il mapping a Unicode con [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)e esegue il mapping a un DBCS diverso con [**WideCharToMultiByte,**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)non sono disponibili garanzie sui risultati. Il carattere originale potrebbe essere mappato a un EUDC diverso nella tabella codici di destinazione oppure potrebbe essere mappato come carattere non definito. Analogamente, il mapping di una stringa Unicode a una tabella codici con un intervallo EUDC può avere risultati imprevisti. Se la stringa Unicode contiene un punto di codice PUA, è possibile che il punto di codice sia mappato a un EUDC che non rappresenta lo stesso carattere.

Le applicazioni possono confrontare stringhe DBCS che contengono EUDC usando la versione ANSI della [funzione CompareString.](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) La funzione esegue in modo efficace il mapping dei caratteri a Unicode prima di confrontare i valori dei caratteri. Le applicazioni possono creare una chiave di ordinamento per la stringa usando la versione ANSI della funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) e il valore \_ LCMAP SORTKEY. Questa funzione esegue in modo efficace il mapping dei caratteri a Unicode. Tutti i caratteri nella pua vengono ordinati dopo tutti gli altri caratteri Unicode. All'interno dell'area i caratteri vengono ordinati in ordine numerico. Se un'applicazione tenta di recuperare informazioni CTYPE per eudc usando la [funzione GetStringTypeA,](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) la funzione recupera **NULL** per ogni carattere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di unicode e set di caratteri](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
