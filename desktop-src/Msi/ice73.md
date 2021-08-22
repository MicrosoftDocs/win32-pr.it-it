---
description: ICE73 verifica che il pacchetto non riutilizzi i codici pacchetto, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK. I pacchetti non devono mai riutilizzare il pacchetto, l'aggiornamento o i codici prodotto di un altro prodotto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e5beecbfc7b4345d3b0dd7a93b86c55acc1abde4cc4f99d72749368be9d303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635077"
---
# <a name="ice73"></a>ICE73

ICE73 verifica che il pacchetto non riutilizzi i codici pacchetto, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK. I pacchetti non devono mai riutilizzare il pacchetto, l'aggiornamento o i codici prodotto di un altro prodotto.

## <a name="result"></a>Risultato

ICE73 genera un avviso se il pacchetto del prodotto riutilizza un pacchetto o un codice prodotto di un esempio sdk Windows Installer.

## <a name="example"></a>Esempio

ICE73 segnala gli errori seguenti per l'esempio illustrato:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Gli asterischi ( \* \* \* ) nel GUID rappresentano l'intervallo di GUID riservati per i Windows \* sdk del programma di installazione.

 

Per correggere gli errori, generare un nuovo GUID univoco per i codici di prodotto e pacchetto del pacchetto. Sarà necessario anche un nuovo GUID univoco per il codice di aggiornamento del pacchetto.

[Flusso di informazioni di riepilogo](summary-information-stream.md) (parziale)



| Proprietà       | Valore                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-000000000047} |



 

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà                           | Valore                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**Codice di aggiornamento**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici dei pacchetti](package-codes.md)
</dt> <dt>

[Codici prodotto](product-codes.md)
</dt> <dt>

[**Proprietà Riepilogo numero revisione**](revision-number-summary.md)
</dt> <dt>

[**Proprietà UpgradeCode**](upgradecode.md)
</dt> <dt>

[**Proprietà ProductCode**](productcode.md)
</dt> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



