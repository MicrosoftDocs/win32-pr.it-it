---
description: ICE73 verifica che il pacchetto non riutilizzi i codici dei pacchetti, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK. I pacchetti non devono mai riutilizzare i codici di pacchetto, aggiornamento o prodotto di un altro prodotto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308325"
---
# <a name="ice73"></a>ICE73

ICE73 verifica che il pacchetto non riutilizzi i codici dei pacchetti, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK. I pacchetti non devono mai riutilizzare i codici di pacchetto, aggiornamento o prodotto di un altro prodotto.

## <a name="result"></a>Risultato

ICE73 genera un avviso se il pacchetto del prodotto riutilizza un pacchetto o un codice prodotto di un esempio SDK Windows Installer.

## <a name="example"></a>Esempio

ICE73 segnala gli errori seguenti per l'esempio illustrato:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Gli asterischi ( \* \* \* \* ) nel GUID rappresentano l'intervallo di GUID riservati per i pacchetti Windows Installer SDK successivi.

 

Per correggere gli errori, generare un nuovo GUID univoco per i codici del prodotto e del pacchetto del pacchetto. Sarà inoltre necessario un nuovo GUID univoco per il codice di aggiornamento del pacchetto.

[Flusso di informazioni di riepilogo](summary-information-stream.md) (parziale)



| Proprietà       | Valore                                  |
|----------------|----------------------------------------|
| \_REVNUMBER PID | {000C1101-0000-0000-C000-000000000047} |



 

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà                           | Valore                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**UpgradeCode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici del pacchetto](package-codes.md)
</dt> <dt>

[Codici prodotto](product-codes.md)
</dt> <dt>

[**Proprietà riepilogo Numero revisione**](revision-number-summary.md)
</dt> <dt>

[**Proprietà UpgradeCode**](upgradecode.md)
</dt> <dt>

[**Proprietà ProductCode**](productcode.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



