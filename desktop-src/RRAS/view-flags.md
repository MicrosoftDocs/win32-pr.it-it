---
title: Visualizzare i flag
description: Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ae9763587cf7972aab3ca9880d5ad26350c3161955c17940484cc1cbd801bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024951"
---
# <a name="view-flags"></a>Visualizzare i flag

Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.



| Costante                 | Valore      | Descrizione                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| DIMENSIONI \_ MASSIME \_ \_ DELL'INDIRIZZO RTM | 16         | Dimensioni massime degli indirizzi per una famiglia di indirizzi.                          |
| VISTE \_ MAX RTM \_          | 32         | Numero massimo di viste che possono essere attive nella tabella di routing. |
| UCAST \_ \_ DELL'ID VISTA \_ RTM     | 0          | Specifica una vista unicast.                                        |
| MCAST \_ \_ DELL'ID DI \_ VISUALIZZAZIONE RTM     | 1          | Specifica una visualizzazione multicast.                                      |
| DIMENSIONI \_ DELLA MASCHERA \_ DI VISUALIZZAZIONE \_ RTM    | 0x20       | Specifica il numero massimo di viste che è possibile configurare.    |
| RTM \_ VIEW \_ MASK \_ NONE    | 0x00000000 | Restituisce informazioni indipendentemente dalla visualizzazione.                      |
| RTM \_ VIEW \_ MASK \_ ANY     | 0x00000000 | Restituisce le destinazioni da tutte le visualizzazioni. Si tratta del valore predefinito.  |
| MASCHERA DI VISUALIZZAZIONE RTM \_ \_ \_ UCAST   | 0x00000001 | Restituisce le destinazioni dalla visualizzazione unicast.                      |
| MCAST \_ DELLA MASCHERA DI VISUALIZZAZIONE \_ \_ RTM   | 0x00000002 | Restituisce le destinazioni dalla visualizzazione multicast.                    |
| RTM \_ VIEW \_ MASK \_ ALL     | 0xffffffff | Restituisce informazioni da tutte le visualizzazioni.                              |



 

 

 




