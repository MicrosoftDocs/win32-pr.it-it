---
description: Le applicazioni scrivono i caratteri definiti dall'utente finale (EUDCs) e i caratteri PUA (private use area) sullo schermo o sulla stampante nello stesso modo in cui scrivono altri caratteri, usando funzioni di output come Text out e ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Scrittura, mapping e ordinamento dei caratteri EUDC e PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226128"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Scrittura, mapping e ordinamento dei caratteri EUDC e PUA

Le applicazioni scrivono i caratteri definiti dall'utente finale (EUDCs) e i caratteri PUA (private use area) sullo schermo o sulla stampante nello stesso modo in cui scrivono altri caratteri, usando funzioni di output come [Text](/windows/win32/api/wingdi/nf-wingdi-textouta) out e [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Queste funzioni recuperano automaticamente informazioni sui caratteri da caratteri carattere EUDC o PUA se EUDC è abilitato. Per ulteriori informazioni, vedere la pagina relativa ai [caratteri definiti dall'utente finale \_ e dall'area uso privato](end-user-defined-characters.md).

Quando si scrivono caratteri EUDCs o PUA, l'operazione della funzione di output di testo dipende dal tipo di carattere correntemente selezionato. Se il tipo di carattere selezionato è un carattere EUDC o PUA integrato, la funzione recupera le informazioni sui caratteri da tale tipo di carattere. Se il tipo di carattere selezionato è un tipo di carattere TrueType DBCS ( [Double-byte character set](double-byte-character-sets.md) ) a cui è associato un tipo di carattere EUDC separato, la funzione recupera le informazioni dal tipo di carattere EUDC specificato. Analogamente, se il tipo di carattere selezionato è un tipo di carattere TrueType [Unicode](unicode.md) a cui è associato un tipo di carattere PUA separato, la funzione recupera le informazioni dal tipo di carattere PUA. Se per il tipo di carattere selezionato non è associato un tipo di carattere EUDC o PUA, la funzione recupera le informazioni dal tipo di carattere EUDC predefinito del sistema. Se il carattere non è presente nel tipo di carattere EUDC predefinito di sistema o se non è presente alcun tipo di carattere EUDC predefinito di sistema, la funzione scrive il carattere predefinito definito dal tipo di carattere selezionato.

Le applicazioni possono eseguire il mapping di EUDCs a e da Unicode usando le funzioni [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) . La funzione **MultiByteToWideChar** esegue il mapping della maggior parte dei EUDCs ai caratteri nel PUA Unicode. Tuttavia, per supportare determinati standard nazionali o regionali, è possibile eseguire il mapping di alcuni EUDCs a punti di codice Unicode non PUA. La funzione **WideCharToMultiByte** esegue il mapping di un carattere in PUA alla relativa controparte EUDC, se tale mapping esiste e se il punto di codice non dispone di un mapping non PUA valido in Unicode. Non tutte le tabelle codici includono un intervallo di EUDC. La tabella codici specificata in una chiamata a **WideCharToMultiByte** deve contenere un intervallo di codice EUDC per l'esecuzione del mapping all'intervallo EUDC. Se la tabella codici non contiene un intervallo di codice EUDC, la funzione recupera il carattere predefinito per tutti i caratteri nel PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) non garantiscono il mapping round trip. In altre parole, è possibile iniziare con una particolare stringa multibyte contenente EUDCs, eseguire il mapping della stringa a Unicode con **MultiByteToWideChar** e mapparla di nuovo al DBCS originale con **WideCharToMultiByte** e finire con un risultato non identico alla stringa originale. Le applicazioni che si basano sul mapping di EUDCs a Unicode devono garantire che tutti i caratteri necessari possano eseguire il round trip tra l'area di EUDC della tabella codici appropriata e il PUA Unicode.

Le applicazioni non devono tentare di eseguire il mapping di EUDCs da una tabella codici a un'altra. Se un'applicazione inizia con un EUDC da una tabella codici, ne esegue il mapping a Unicode con [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)e viene mappata a un DBCS diverso con [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte), non sono previste garanzie sui risultati. Il carattere originale potrebbe essere mappato a un EUDC diverso nella tabella codici di destinazione o potrebbe essere mappato come carattere non definito. Analogamente, il mapping di una stringa Unicode a una tabella codici con un intervallo di EUDC può avere risultati imprevisti. Se la stringa Unicode contiene un punto di codice PUA, è possibile che il punto di codice venga mappato a un EUDC che non rappresenta lo stesso carattere.

Le applicazioni possono confrontare le stringhe DBCS che contengono EUDCs usando la versione ANSI della funzione [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) . La funzione esegue il mapping dei caratteri a Unicode prima di confrontare i valori dei caratteri. Le applicazioni possono creare una chiave di ordinamento per la stringa usando la versione ANSI della funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) e il \_ valore LCMAP SORTKEY. Questa funzione esegue in modo efficace il mapping di caratteri a Unicode. Tutti i caratteri in PUA vengono ordinati dopo tutti gli altri caratteri Unicode. All'interno dell'area, i caratteri vengono ordinati in ordine numerico. Se un'applicazione tenta di recuperare informazioni CTYPE per un EUDC tramite la funzione [GetStringTypeA](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) , la funzione recupera il **valore null** per ogni carattere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
