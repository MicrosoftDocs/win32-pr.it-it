---
description: 'Windows Vista e versioni successive: NLS definisce diverse pseudo-impostazioni locali da utilizzare oltre alle impostazioni locali di Windows esistenti.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306604"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista e versioni successive:** NLS definisce diverse pseudo-impostazioni locali da utilizzare oltre alle impostazioni locali di Windows esistenti. Usare queste pseudo-impostazioni locali per testare la localizzazione delle applicazioni. Per informazioni dettagliate sull'implementazione, vedere [uso di Pseudo-Locales per il test di localizzazione](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Pseudo-Locales supportati

Le pseudo-impostazioni locali supportate da NLS sono:

-   Pseudo-impostazioni locali di base
-   Pseudo-impostazioni locali con mirroring (da destra a sinistra)
-   Lingue asiatiche orientali-pseudo-impostazioni locali

Scegliere le specifiche pseudo-impostazioni locali da usare in base alle assegnazioni della tabella codici e alle stringhe per la localizzazione, ad esempio i nomi dei mesi e dei giorni. I dati per ogni pseudo-impostazioni locali includono non solo le tabelle codici pertinenti e le stringhe giorno e mese per la localizzazione, ma anche i dati per diversi altri test case per NLS. I test case esaminano i tipi di dati seguenti:

-   [identificatori delle impostazioni locali](locale-identifiers.md)a 9 bit. Le pseudo-impostazioni locali offrono la possibilità di testare il funzionamento degli identificatori delle impostazioni locali a 9 bit.
-   Stringhe da linguaggi che devono usare tipi di carattere piccoli. A causa delle limitazioni nell'interfaccia GDI (Graphics Device Interface), il tipo di carattere dell'interfaccia utente per alcune lingue è più piccolo di quello ottimale. Le pseudo-impostazioni locali includono diverse stringhe di questi linguaggi, combinate con stringhe da linguaggi con una gestione dei tipi di carattere più standard. È possibile utilizzare queste stringhe nei test per determinare come viene eseguito il rendering di un tipo di carattere limitato da GDI.
-   Lunghezze di stringa insolite. Alcune costanti di informazioni sulle impostazioni locali, ad esempio [ \_ slist](locale-slist.md) delle impostazioni locali e [ \_ ICURRENCY delle impostazioni locali](locale-icurrency.md), presentano limiti convenzionali sulle dimensioni della stringa. Le pseudo-impostazioni locali supportano l'esame delle diverse lunghezze di stringa.
-   Ordinamenti alternativi. Le pseudo-impostazioni locali possono essere usate per testare la funzionalità di ordinamento alternativo quando l' [identificatore](sort-order-identifiers.md) di ordinamento alternativo è diverso dall'identificatore di ordinamento di base che in genere è associato alle impostazioni locali.

## <a name="pseudo-locale-names-and-identifiers"></a>Identificatori e nomi di pseudo-impostazioni locali

Le pseudo-impostazioni locali hanno [nomi di impostazioni locali](locale-names.md) scelti dallo spazio di utilizzo privato per evitare conflitti con le stringhe possibili introdotte negli standard organizzazione internazionale per la standardizzazione (iso) 639 e ISO 3166. Ogni pseudo-impostazioni locali dispone anche di un proprio identificatore delle impostazioni locali. Nella tabella seguente sono riportati i nomi e gli identificatori per le pseudo-impostazioni locali definite.



| Pseudo-impostazioni locali       | Nome delle impostazioni locali | Identificatore delle impostazioni locali |
|---------------------|-------------|-------------------|
| Base                | query al secondo-ploc    | 0501              |
| Con mirroring            | query al secondo-plocm   | 09ff              |
| Asia orientale-lingua | query al secondo-Besca   | 05fe              |



 

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato il testo visualizzato per le pseudo-impostazioni locali di base:

\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Identificatori delle impostazioni locali](locale-identifiers.md)
</dt> <dt>

[Nomi delle impostazioni locali](locale-names.md)
</dt> <dt>

[Identificatori di ordinamento](sort-order-identifiers.md)
</dt> <dt>

[Uso di Pseudo-Locales per il test di localizzazione](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



