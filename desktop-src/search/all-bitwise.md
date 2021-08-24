---
description: Le parole chiave ALL BITWISE e SOME BITWISE vengono usate per testare i bit in un tipo integrale.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL BITWISE e SOME BITWISE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594721"
---
# <a name="all-bitwise-and-some-bitwise"></a>ALL BITWISE e SOME BITWISE

Le **parole chiave ALL BITWISE** e SOME **BITWISE** vengono usate per testare i bit in un tipo integrale. Se tutti i bit impostati in una proprietà corrispondono alla maschera, **ALL BITWISE** è true. Se almeno uno dei bit impostati in una proprietà corrisponde alla maschera, **SOME BITWISE** è true.

Gli operatori possono essere applicati sia alle proprietà scalari (a valore singolo) che alle proprietà vettoriali (a più valori). Nell'esempio di codice seguente viene illustrato come testare i valori delle proprietà **con ALL BITWISE** e **SOME BITWISE**.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Operatori di confronto

Gli operatori di confronto supportati per i test BITWISE sono elencati nella tabella seguente.



| Operatore di confronto | Descrizione  |
|---------------------|--------------|
| =                   | Uguale a     |
| != o <>      | Diverso da |



 

La logica dei test BITWISE è elencata nella tabella seguente.



| Operatore di test e confronto BITWISE | Logica                   |
|--------------------------------------|-------------------------|
| = ALL BIT PER BIT                        | Maschera & proprietà = Maschera  |
| = ALCUNI BIT PER BIT                       | Proprietà & Mask != 0    |
| <> TUTTI BIT PER BIT                 | Maschera & proprietà != Maschera |
| <> ALCUNI BIT PER BIT                | Maschera & proprietà = 0     |



 

Nella tabella seguente vengono utilizzati valori binari ed esadecimali di esempio per eseguire test BITWISE.



| Proprietà in formato binario (esadecimale) | Maschera in formato binario (esadecimale) | Maschera & proprietà = binario (esadecimale) | = ALCUNI BIT PER BIT | = ALL BIT PER BIT |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Vero           | Falso         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | False          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | False          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | Vero           | Falso         |



 

## <a name="example"></a>Esempio

Di seguito è riportato un esempio del **predicato ALL BITWISE.**


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



