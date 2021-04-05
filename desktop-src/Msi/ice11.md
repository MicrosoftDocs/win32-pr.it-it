---
description: ICE11 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere installazioni simultanee.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967793"
---
# <a name="ice11"></a>ICE11

ICE11 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

## <a name="result"></a>Risultato

ICE11 convalida la colonna di origine della [tabella CustomAction](customaction-table.md) delle azioni personalizzate di installazione simultanea. La colonna di origine deve contenere un [GUID](guid.md) valido (Codice prodotto MSI).

ICE11 Invia un errore se la colonna di origine della tabella CustomAction non è stata creata correttamente per le azioni personalizzate di installazione simultanea.

## <a name="example"></a>Esempio

ICE inserisce i messaggi di errore seguenti per l'esempio illustrato.

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



 

Per correggere gli errori, per CA1 non è possibile eseguire un'installazione simultanea del "pacchetto di base". Ciò comporta un'installazione ricorsiva. Questa voce deve essere rimossa o la colonna di origine deve essere modificata in un GUID per un file MSI annunciato che differisce dal GUID del pacchetto di base. Per il CA2, fare in modo che tutti i caratteri del GUID siano maiuscoli. Infine, modificare la colonna di origine CA4's per fare riferimento a un GUID valido di un file MSI annunciato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazioni simultanee](concurrent-installations.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



