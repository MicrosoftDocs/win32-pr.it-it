---
description: 'Windows Vista e versioni successive: NLS definisce diverse pseudo-impostazioni locali da usare oltre alle impostazioni locali Windows esistenti.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e099ee2af283c38aff3de7813fec64b5d43c6ac5873549856b27fd224c3e0d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390415"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista e versioni successive:** NLS definisce diverse pseudo-impostazioni locali da usare oltre alle impostazioni locali Windows esistenti. Usare queste pseudo-impostazioni locali per testare la localizzazione delle applicazioni. Per informazioni dettagliate sull'implementazione, vedere [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Funzionalità Pseudo-Locales

Le pseudo-impostazioni locali supportate da NLS sono:

-   Pseudo-impostazioni locali di base
-   Pseudo-impostazioni locali con mirroring (da destra a sinistra)
-   Pseudo-impostazioni locali della lingua dell'Asia orientale

Scegliere le pseudo-impostazioni locali specifiche da usare in base alle assegnazioni della tabella codici e alle stringhe per la localizzazione, ad esempio i nomi dei mesi e dei giorni. I dati per ogni pseudo-impostazioni locali includono non solo le code pages rilevanti e le stringhe di giorno e mese per la localizzazione, ma anche i dati per diversi altri test case per NLS. I test case esaminano i tipi di dati seguenti:

-   Identificatori delle impostazioni locali [a](locale-identifiers.md)9 bit. Le pseudo-impostazioni locali offrono una buona opportunità per testare il funzionamento degli identificatori delle impostazioni locali a 9 bit.
-   Stringhe di lingue che devono usare tipi di carattere di piccole dimensioni. A causa delle limitazioni dell'interfaccia GDI (Graphics Device Interface), il tipo di carattere dell'interfaccia utente per alcune lingue è inferiore a quello ottimale. Le pseudo-impostazioni locali includono diverse stringhe di queste lingue, combinate con stringhe di lingue con una gestione dei caratteri più standard. È possibile usare queste stringhe nei test per determinare il modo in cui viene eseguito il rendering di un tipo di carattere con limiti GDI.
-   Lunghezze di stringa insolite. Alcune costanti di informazioni sulle impostazioni locali, ad esempio [LOCALE \_ SLIST](locale-slist.md) e [LOCALE \_ ICURRENCY,](locale-icurrency.md)hanno limiti convenzionali per le dimensioni delle stringhe. Le pseudo-impostazioni locali supportano l'esame di lunghezze di stringa diverse.
-   Ordinamenti alternativi. Le pseudo-impostazioni locali possono essere usate per [](sort-order-identifiers.md) testare la funzionalità di ordinamento alternativa quando l'identificatore di ordinamento alternativo è diverso dall'identificatore dell'ordinamento di base in genere associato alle impostazioni locali.

## <a name="pseudo-locale-names-and-identifiers"></a>Nomi e identificatori delle pseudo-impostazioni locali

Le pseudo-impostazioni [](locale-names.md) locali hanno nomi di impostazioni locali scelti dallo spazio di utilizzo privato per evitare conflitti con le possibili stringhe introdotte negli standard International Organization for Standardization (ISO) 639 e ISO 3166. Ogni pseudo-impostazioni locali ha anche un proprio identificatore delle impostazioni locali. Nella tabella seguente vengono forniti i nomi e gli identificatori per le pseudo-impostazioni locali definite.



| Pseudo-impostazioni locali       | Nome delle impostazioni locali | Identificatore delle impostazioni locali |
|---------------------|-------------|-------------------|
| Base                | qps-ploc    | 0501              |
| Con mirroring            | qps-plocm   | 09ff              |
| Lingua dell'Asia orientale | qps-ploca   | 05fe              |



 

## <a name="example"></a>Esempio

L'esempio seguente mostra il testo visualizzato per una pseudo-impostazioni locali di base:

\[Шěđлеśđαỳ !!! , \] 8 òf \[ Μäŕςћ !! \] âf 2006

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

[Uso Pseudo-Locales per i test di localizzazione](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



