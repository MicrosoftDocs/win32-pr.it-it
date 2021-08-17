---
description: Il codice prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Codici prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2afe0c96e78d14bc989d4acdc7195d374b82466c4b345a999df7085468587e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145374"
---
# <a name="product-codes"></a>Codici prodotto

Il codice prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Per altre informazioni, vedere la [**proprietà ProductCode.**](productcode.md) Se vengono apportate modifiche significative a un prodotto, è necessario modificare anche il codice del prodotto per riflettere questa impostazione. Non è tuttavia un requisito che il codice del prodotto sia modificato se le modifiche al prodotto sono relativamente minori.

Le versioni a 32 bit e a 64 bit del pacchetto di un'applicazione devono avere codici di prodotto diversi. Se un componente a 32 bit di un'applicazione viene ricompilato in un componente a 64 bit, è necessario assegnare un nuovo codice prodotto.

Se un server esposto nella tabella [PublishComponent](publishcomponent-table.md) viene ricompilato da 32 bit a 64 bit, potrebbe essere necessario modificare anche il GUID in questa tabella in modo che i client a 32 bit e a 64 bit possano identificare la categoria di componenti qualificati appropriata. In questo caso, è necessario modificare anche il codice del prodotto.

Si noti che le lettere nei GUID del codice prodotto devono essere maiuscole. Utilità come GUIDGEN generano GUID contenenti lettere minuscole. Le lettere minuscole in questi GUID devono essere modificate in lettere maiuscole per essere usate come codice prodotto o codice pacchetto. Per altre informazioni, vedere [Modifica del codice prodotto.](changing-the-product-code.md)

Il codice del pacchetto è un GUID che identifica un particolare Windows programma di [*installazione .*](p-gly.md) Il codice del pacchetto associa un file .msi a un'applicazione o a un prodotto e può essere usato anche per la verifica delle origini. I codici prodotto e pacchetto non sono intercambiabili. Due file non .msi non devono mai avere lo stesso codice del pacchetto. Anche se è comune spedire un'applicazione con lo stesso codice pacchetto e codice prodotto, i due valori possono divergere quando l'applicazione viene aggiornata. Per altre informazioni, vedere [Codici pacchetto.](package-codes.md)

 

 



