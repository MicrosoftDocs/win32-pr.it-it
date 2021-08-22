---
description: ICE11 viene usato con installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere Installazioni simultanee.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6e578cd6f7da09cc1894bc154ba77225f1efaafedf45f3fb7cdd3f30190e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119296491"
---
# <a name="ice11"></a>ICE11

ICE11 viene usato con installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [Installazioni simultanee](concurrent-installations.md).

## <a name="result"></a>Risultato

ICE11 convalida la colonna Source della tabella [CustomAction delle](customaction-table.md) azioni personalizzate di installazione simultanea. La colonna Source deve contenere un [GUID](guid.md) valido (codice prodotto MSI).

ICE11 invia un errore se la colonna Source della tabella CustomAction viene creato in modo non corretto per le azioni personalizzate di installazione simultanea.

## <a name="example"></a>Esempio

ICE pubblica i messaggi di errore seguenti per l'esempio illustrato.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà        | Valore                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[Tabella CustomAction](customaction-table.md) (parziale)



| CustomAction | Tipo | Source (Sorgente)                                 |
|--------------|------|----------------------------------------|
| CA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Per correggere gli errori, per CA1 non è possibile eseguire un'installazione simultanea del "pacchetto di base". Ciò comporta un'installazione ricorsiva. Questa voce deve essere rimossa o la colonna Source deve essere modificata in un GUID per un file MSI annunciato diverso dal GUID del pacchetto di base. Per CA2, impostare tutti i caratteri del GUID in maiuscolo. Modificare infine la colonna Source di CA4 in modo da fare riferimento a un GUID valido di un'istanza di MSI annunciata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazioni simultanee](concurrent-installations.md)
</dt> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



