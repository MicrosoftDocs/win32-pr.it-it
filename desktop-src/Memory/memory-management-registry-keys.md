---
description: Lo spazio dell'indirizzo virtuale di sistema (VA) nei sistemi a 32 bit può esaurirsi a causa della frammentazione. È possibile utilizzare diverse chiavi del registro di sistema per configurare i limiti di memoria nei sistemi a 32 bit in cui si verifica questo problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Chiavi del registro di sistema di gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885709"
---
# <a name="memory-management-registry-keys"></a>Chiavi del registro di sistema di gestione della memoria

Lo spazio dell'indirizzo virtuale di sistema (VA) nei sistemi a 32 bit può esaurirsi a causa della frammentazione. È possibile utilizzare diverse chiavi del registro di sistema per configurare i limiti di memoria nei sistemi a 32 bit in cui si verifica questo problema. Lo spazio di sistema VA nei sistemi a 64 bit non è soggetto all'esaurimento della frammentazione. Pertanto, queste chiavi non hanno alcun effetto sui sistemi a 64 bit.

Per i sistemi a 32 bit, queste chiavi del registro di sistema di gestione della memoria devono essere create in modo esplicito nella seguente chiave del registro di sistema:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Gestione della memoria** del controllo del sistema di gestione delle sessioni del computer locale

**Windows Server 2008 e Windows Vista:** Queste chiavi del registro di sistema sono disponibili nei sistemi a 32 bit a partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

Per i limiti di memoria e spazio degli indirizzi predefiniti per i sistemi a 32 bit e a 64 bit, vedere [limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md).

La tabella seguente descrive le chiavi del registro di sistema di gestione della memoria che possono essere usate per configurare i limiti di memoria nei sistemi a 32 bit. Tutte queste chiavi hanno un tipo REG \_ DWORD e i valori possibili sono compresi tra 0 e 2.048 MB. Il valore predefinito è 0, che indica che non viene applicato alcun limite. I valori vengono arrotondati automaticamente per eccesso al limite di allocazione del sistema successivo, ovvero 2 MB nei sistemi a 32 bit con [estensione di indirizzo fisico](physical-address-extension.md) (PAE) abilitata e 4 MB su sistemi a 32 bit in cui non è abilitata la funzionalità PAE.



| Chiave                   | Descrizione                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | Specifica la quantità massima di spazio VA del sistema che può essere utilizzato dal pool non di paging. In determinate condizioni, questo limite può essere superato da un importo ridotto. |
| **PagedPoolLimit**    | Specifica la quantità massima di spazio VA del sistema che può essere utilizzato dal pool di paging.                                                                            |
| **SessionSpaceLimit** | Specifica la quantità massima di spazio VA del sistema che può essere usata dalle allocazioni dello spazio di sessione.                                                                 |
| **SystemCacheLimit**  | Specifica la quantità massima di spazio VA del sistema che può essere usata dalla cache di sistema. In determinate condizioni, questo limite può essere superato da un importo ridotto.  |
| **SystemPtesLimit**   | Specifica la quantità massima di spazio di sistema che può essere utilizzato dai mapping I/O e da altre risorse che utilizzano le voci della tabella delle pagine di sistema (PTE).            |



 

Per determinare se lo spazio di sistema VA esaurito, è necessario usare un debugger del kernel. Per altre informazioni, vedere [Strumenti di debug per Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



