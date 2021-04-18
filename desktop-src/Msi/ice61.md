---
description: ICE61 convalida la tabella di aggiornamento di un database di Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314792"
---
# <a name="ice61"></a>ICE61

ICE61 controlla la tabella di aggiornamento per verificare che siano soddisfatte le condizioni seguenti:

-   Tutte le proprietà di ActionProperty non sono già state create nella tabella delle proprietà.
-   Tutte le proprietà di ActionProperty sono proprietà pubbliche.
-   Tutte le proprietà di ActionProperty sono incluse nella proprietà [**SecureCustomProperties**](securecustomproperties.md) .
-   Tutte le proprietà di ActionProperty sono univoche per ogni record della tabella di aggiornamento.
-   Tutti i valori di VersionMax non sono minori dei valori VersionMin corrispondenti.
-   I valori VersionMin e VersionMax sono versioni di prodotti valide. Per il formato della versione del prodotto valido, vedere la proprietà [**ProductVersion**](productversion.md) .
-   Non viene effettuato alcun tentativo di rimuovere una versione più recente o uguale del prodotto corrente.

La mancata correzione di un avviso o di un errore segnalato da ICE61 in genere comporta problemi nell'aggiornamento dell'applicazione. A seconda dell'errore esatto, potrebbe essere necessario lasciare i file dalla versione precedente, eliminare i file dalla versione precedente anche se sono necessari per la nuova applicazione o completare l'errore dell'aggiornamento.

## <a name="result"></a>Risultato

ICE61 Invia un avviso o un errore se una qualsiasi delle condizioni precedenti non è vera.

## <a name="example"></a>Esempio

ICE61 segnala gli errori e gli avvisi seguenti per gli esempi mostrati.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

In questo caso, la prima riga tenterà di rimuovere un prodotto della stessa versione. La colonna VersionMax è uguale alla versione del prodotto nella tabella delle proprietà.

Per correggere l'errore, utilizzare una versione nella colonna VersionMax inferiore alla versione corrente specificata nella tabella delle proprietà. Rimuovere il bit **msidbUpgradeAttributesVersionMaxInclusive** dalla colonna Attributes se VersionMax è uguale alla versione corrente. Se lo scopo è quello di rilevare il prodotto e non rimuoverlo, l'errore verrà risolto anche aggiungendo il bit **msidbUpgradeAttributesOnlyDetect** alla colonna Attributes.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A meno che la proprietà non sia elencata nella proprietà [**SecureCustomProperties**](securecustomproperties.md) , la proprietà non viene passata al lato server dell'installazione quando viene trovata la proprietà.

Per correggere l'errore, aggiungere la proprietà a [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Le proprietà di aggiornamento devono essere proprietà pubbliche affinché il risultato venga passato al lato server dell'installazione.

Per correggere l'errore, utilizzare tutte le lettere maiuscole nel nome della proprietà.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Una proprietà può essere utilizzata solo in una riga della tabella di aggiornamento.

Per correggere l'errore, utilizzare una proprietà diversa per la seconda riga.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

La versione minima deve essere minore della versione massima.

Per correggere l'errore, controllare i numeri di versione per gli errori di digitazione. Se sono corretti e si vuole usare l'intervallo tra le due versioni, cambiarle in modo che VersionMin sia minore di VersionMax.

[Tabella delle proprietà](property-table.md)



| Proprietà                                                 | Valore                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Aggiorna tabella](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Linguaggio | Attributi | Rimuovi                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



