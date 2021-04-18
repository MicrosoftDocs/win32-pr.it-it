---
description: L'arabo e molti altri linguaggi hanno forme classiche per i numeri diversi dalle cifre occidentali convenzionali più spesso usate nei computer.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Forme cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317170"
---
# <a name="digit-shapes"></a>Forme cifre

L'arabo e molti altri linguaggi hanno forme classiche per i numeri diversi dalle cifre occidentali convenzionali più spesso usate nei computer. Per evitare ambiguità nella denominazione di queste forme, in questo documento vengono utilizzati i nomi seguenti dello standard Unicode.



| Nome Unicode delle cifre                                     | Paese/area geografica in cui sono stati usati                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Cifre europee                                                | Europa, Americhe e molti altri paesi/aree geografiche       |
| Cifre Arabic-Indic                                            | Paesi/aree Arabi (sebbene molti usino cifre europee) |
| Altre cifre nazionali: cifre indiane, cifre tailandesi e simili | Diversi paesi/aree geografiche                                    |



 

Unicode fornisce punti di codice separati per ogni forma di cifra. Quindi, per accedere alle forme speciali di cifre della lingua, l'applicazione può usare i codici carattere Unicode pertinenti per le cifre precedenti, U + 0030 a U + 0039. Questi codici vengono sempre visualizzati con la forma appropriata, in base alla disponibilità dei tipi di carattere.

I codici carattere Unicode U + 0030 a U + 0039 rappresentano nominalmente i numeri europei da 0 a 9, ma la relativa forma digit può essere modificata. Le API di testo GDI e DirectWrite forniscono meccanismi che consentono alle applicazioni di controllare questo comportamento. Vedere, ad esempio, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) o [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution). Il comportamento in alcuni controlli della shell e nei framework dell'interfaccia utente può rispondere alle impostazioni locali dell'utente per la sostituzione delle cifre. le impostazioni [locali \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCType possono essere usate per ottenere le impostazioni di sostituzione cifre predefinite per le diverse impostazioni locali o le impostazioni desktop dell'utente corrente per la sostituzione delle cifre.

## <a name="native-digits"></a>Cifre native

Le cifre native sono le forme cifra scelte dall'utente nella finestra delle proprietà **numero** nella parte opzioni internazionali e della lingua del pannello di controllo. Per trovare la presentazione dei numeri preferita dall'utente, l'applicazione usa la funzione [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [ \_ SNATIVEDIGITS delle impostazioni](locale-snative-constants.md) locali che rappresenta le informazioni sulle impostazioni locali.

> [!Note]  
> In genere, i codici cifra Unicode vengono generati nelle routine del sistema operativo in fase di esecuzione. Pertanto, è necessario aggiornare i sistemi operativi di runtime comuni affinché l'applicazione esamini le [impostazioni locali \_ SNATIVEDIGITS](locale-snative-constants.md) in modo appropriato.

 

## <a name="digit-substitution"></a>Sostituzione cifre

L'applicazione può usare la sostituzione dei numeri per indicare al sistema operativo come stampare le cifre U + 0030 fino a U + 0039. La costante [ \_ IDIGITSUBSTITUTION delle impostazioni locali](locale-idigitsubstitution.md) controlla questa operazione.

## <a name="digit-shaping-for-a-single-function"></a>Shaping dei numeri per una singola funzione

Le funzioni [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)e [GCP \_ results](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) hanno flag che regolano la sostituzione dei codici Unicode U + 0030 fino a u + 0039 per la durata della chiamata di funzione. Questi flag sostituiscono le impostazioni internazionali nel pannello di controllo, ma non reimpostano le impostazioni. Inoltre, non eseguono l'override dei codici Unicode e dei relativi nodi. Sono disponibili i flag seguenti.



| Flags                 | Cifre utilizzate                      | Campo di utilizzo                   |
|-----------------------|----------------------------------|---------------------------|
| \_NUMERICSLATIN Eto    | Cifre europee                  | **ExtTextOut**            |
| \_NUMERICSLOCAL Eto    | Cifre appropriate per le impostazioni locali | **ExtTextOut**            |
| \_NUMERICSLATIN GCP    | Cifre europee                  | **GetCharacterPlacement** |
| \_NUMERICSLOCAL GCP    | Cifre appropriate per le impostazioni locali | **GetCharacterPlacement** |
| \_LATINNUMBER GCPCLASS | Cifre europee                  | **risultati di GCP \_**          |
| \_LOCALNUMBER GCPCLASS | Cifre appropriate per le impostazioni locali | **risultati di GCP \_**          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
