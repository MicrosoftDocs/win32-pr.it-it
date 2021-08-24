---
description: ICE61 convalida la tabella Upgrade di un database Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c772a076decaa385d01047daa45871aeeaf7898d4cf3347606c4066d1f7f2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580981"
---
# <a name="ice61"></a>ICE61

ICE61 controlla la tabella di aggiornamento per assicurarsi che siano soddisfatte le condizioni seguenti:

-   Tutte le proprietà ActionProperty non vengono pre-creati nella tabella Proprietà.
-   Tutte le proprietà ActionProperty sono Proprietà pubbliche.
-   Tutte le proprietà ActionProperty sono incluse nella [**proprietà SecureCustomProperties.**](securecustomproperties.md)
-   Tutte le proprietà ActionProperty sono univoche per ogni record nella tabella Upgrade.
-   Tutti i valori VersionMax non sono minori dei valori VersionMin corrispondenti.
-   I valori VersionMin e VersionMax sono versioni valide del prodotto. Vedere la [**proprietà ProductVersion**](productversion.md) per il formato di versione del prodotto valido.
-   Non viene effettuato alcun tentativo di rimuovere una versione più recente o uguale del prodotto corrente.

La mancata correzione di un avviso o di un errore segnalato da ICE61 causa in genere problemi durante l'aggiornamento dell'applicazione. A seconda dell'errore esatto, potrebbe essere possibile lasciare i file dalla versione precedente, eliminare i file dalla versione precedente anche se sono necessari per la nuova applicazione o completare l'errore dell'aggiornamento.

## <a name="result"></a>Risultato

ICE61 invia un avviso o un errore se una delle condizioni precedenti non è vera.

## <a name="example"></a>Esempio

ICE61 segnala gli errori e gli avvisi seguenti per gli esempi illustrati.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

In questo caso, la prima riga tenta di rimuovere un prodotto della stessa versione. La colonna VersionMax è uguale alla versione del prodotto nella tabella Proprietà.

Per correggere l'errore, usare una versione nella colonna VersionMax inferiore alla versione corrente specificata nella tabella Property. Rimuovere il bit **msidbUpgradeAttributesVersionMaxInclusive** dalla colonna Attributi se VersionMax è uguale alla versione corrente. Se lo scopo è solo rilevare il prodotto e non rimuoverlo, l'aggiunta del bit **msidbUpgradeAttributesOnlyDetect** alla colonna Attributes correggerà anche questo errore.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A meno che la proprietà non sia elencata nella proprietà [**SecureCustomProperties,**](securecustomproperties.md) la proprietà non viene passata al lato server dell'installazione quando viene trovata la proprietà .

Per correggere l'errore, aggiungere la proprietà a [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Le proprietà di aggiornamento devono essere proprietà pubbliche perché il risultato sia passato al lato server dell'installazione.

Per correggere l'errore, usare tutte le lettere maiuscole nel nome della proprietà.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Una proprietà può essere usata solo in una riga della tabella Upgrade.

Per correggere l'errore, usare una proprietà diversa per la seconda riga.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

La versione minima deve essere minore della versione massima.

Per correggere l'errore, verificare la presenza di errori di digitazione nei numeri di versione. Se sono corrette e si vuole usare l'intervallo tra le due versioni, cambiarle in modo che VersionMin sia minore di VersionMax.

[Tabella delle proprietà](property-table.md)



| Proprietà                                                 | Valore                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Aggiornare la tabella](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Linguaggio | Attributi | Rimuovi                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



