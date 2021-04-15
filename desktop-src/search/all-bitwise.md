---
description: TUTTE le parole chiave bit per bit and bit per bit vengono usate per il testing dei bit in un tipo integrale.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL bit per bit e SOME bit per bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525471"
---
# <a name="all-bitwise-and-some-bitwise"></a>ALL bit per bit e SOME bit per bit

**Tutte** le parole chiave bit per bit **and bit per** bit vengono usate per il testing dei bit in un tipo integrale. Se tutti i bit impostati in una proprietà corrispondono alla maschera, **All bit per bit** è true. Se almeno uno dei bit impostati in una proprietà corrisponde alla maschera, **some bit per bit** è true.

Gli operatori possono essere applicati sia alle proprietà scalari (a valore singolo) che alle proprietà Vector (multiple-value). Nell'esempio di codice seguente viene illustrato come testare i valori delle proprietà con **tutti gli operatori bit per bit** e **bit per bit**.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Operatori di confronto

Nella tabella seguente sono elencati gli operatori di confronto supportati per i test bit per bit.



| Operatore di confronto | Descrizione  |
|---------------------|--------------|
| =                   | Uguale a     |
| ! = o <>      | Diverso da |



 

La logica dei test bit per bit è elencata nella tabella seguente.



| Operatore di confronto e test bit per bit | Logica                   |
|--------------------------------------|-------------------------|
| = TUTTO BIT PER BIT                        | Proprietà & mask = mask  |
| = SOME BIT PER BIT                       | Proprietà & mask! = 0    |
| <> BIT PER BIT                 | Proprietà & mask! = mask |
| <> BIT PER BIT                | Proprietà & mask = 0     |



 

La tabella di verità seguente usa i valori binari e esadecimali di esempio per demonstate la logica dei test bit per bit.



| Property in Binary (hex) | Maschera in binario (esadecimale) | Property & mask = Binary (hex) | = SOME BIT PER BIT | = TUTTO BIT PER BIT |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Vero           | Falso         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | False          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | False          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | Vero           | Falso         |



 

## <a name="example"></a>Esempio

Di seguito è riportato un esempio del predicato **All bit per bit** .


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

 

 



