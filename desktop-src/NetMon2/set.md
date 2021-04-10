---
description: La struttura del SET definisce un set di valori.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: IMPOSTA struttura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231533"
---
# <a name="set-structure"></a>IMPOSTA struttura

La struttura del **set** definisce un set di valori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Numero totale di voci in un set.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Puntatore a una matrice di valori di BYTE.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Puntatore a una matrice di valori di WORD.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Puntatore a una matrice di valori DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Puntatore a una matrice di strutture [largeInt](largeint.md) .

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Puntatore a una matrice di valori SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Puntatore a una matrice di strutture di [ \_ byte con etichetta](labeled-byte.md) . Ogni struttura di **\_ byte con etichetta** definisce un valore e un'etichetta. Network Monitor visualizza un'etichetta se trova un valore corrispondente nel pacchetto del protocollo.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Puntatore a una matrice di strutture di [ \_ Word con etichetta](labeled-word.md) che definiscono un set di valori di Word ed etichette.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Puntatore a una matrice di strutture [ \_ DWORD con etichetta](labeled-dword.md) che definiscono un set di valori DWORD ed etichette.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Puntatore a una matrice di strutture [ \_ largeInt con etichetta](labeled-largeint.md) che definiscono un set di valori largeInt ed etichette.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Puntatore a una matrice di strutture [ \_ SYSTEMTIME con etichetta](labeled-systemtime.md) che definiscono un set di valori di sistema ed etichette.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Puntatore a una matrice di strutture di [ \_ bit con etichetta](labeled-bit.md) che definiscono un set di coppie di bit con etichetta. Ogni BIT può specificare due etichette un'etichetta per ogni stato (0 o 1) del BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Puntatore a una matrice di valori.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura del **set** viene utilizzata per definire un set di dati di confronto che Network Monitor possibile utilizzare per interpretare il valore di una proprietà in un pacchetto di protocollo. Quando è necessario un set di dati di confronto, nel membro **lpSet** della struttura [PROPERTYINFO](propertyinfo.md) viene specificato un puntatore alla struttura del **set** .

La DLL del parser può fornire un set di valori e un set di etichette. Il membro dell' **Unione** selezionato in una struttura **set** punta a una matrice di strutture che definiscono ogni membro di un set.

-   Valore impostato

    Un set di valori viene utilizzato quando si desidera che Network Monitor includa un indicatore set o not-in set con il valore trovato nel pacchetto del protocollo. Se, ad esempio, viene specificato un set DWORD, Network Monitor visualizza un'etichetta per ogni valore DWORD trovato nel pacchetto di protocollo, che indica che il valore DWORD è o non è specificato nel set.

    Un set di valori può essere basato sui tipi di dati BYTE, WORD, DWORD, LARGEINT e SYSTEMTIME.

-   Set di etichette

    Viene utilizzato un set di etichette quando si desidera che Network Monitor visualizzi un'etichetta definita dall'utente anziché i valori di proprietà specificati in un set.

    Un set di etichette può essere basato sulle coppie BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME e BIT Label.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[con etichetta \_ bit](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




