---
description: La struttura SET definisce un set di valori.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: Struttura SET (Netmon.h)
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
ms.openlocfilehash: d66ba5dd3a977967d0020a00d5813c3f689142b1e58c631c99f9bd10fceba3ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074401"
---
# <a name="set-structure"></a>Struttura SET

La **struttura SET** definisce un set di valori.

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

Puntatore a una matrice di valori BYTE.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Puntatore a una matrice di valori WORD.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Puntatore a una matrice di valori DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Puntatore a una matrice [di strutture LARGEINT.](largeint.md)

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Puntatore a una matrice di valori SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Puntatore a una matrice [di strutture LABELED \_ BYTE.](labeled-byte.md) Ogni **struttura LABELED \_ BYTE** definisce un valore e un'etichetta. Network Monitor un'etichetta se trova un valore corrispondente nel pacchetto del protocollo.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Puntatore a una matrice di [strutture LABELED \_ WORD](labeled-word.md) che definiscono un set di valori ed etichette WORD.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Puntatore a una matrice di [strutture \_ DWORD ETICHETTATE](labeled-dword.md) che definiscono un set di valori ed etichette DWORD.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Puntatore a una matrice di [strutture \_ LABELED LARGEINT](labeled-largeint.md) che definiscono un set di valori ED ETICHETTE LARGEINT.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Puntatore a una matrice di [strutture \_ LABELED SYSTEMTIME](labeled-systemtime.md) che definiscono un set di valori ed etichette SYSTEM.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Puntatore a una matrice di [strutture LABELED \_ BIT](labeled-bit.md) che definiscono un set di coppie BIT etichettate. Ogni BIT può specificare due etichette un'etichetta per ogni stato (0 o 1) del BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Puntatore a una matrice di valori.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura SET** viene usata per definire un set di dati di confronto che Network Monitor possibile usare per interpretare il valore di una proprietà in un pacchetto di protocollo. Quando è necessario un set di dati di confronto, viene specificato un puntatore alla struttura **SET** nel membro **lpSet** della [struttura PROPERTYINFO.](propertyinfo.md)

La DLL del parser può fornire un set di valori e un set di etichette. Il membro **dell'istruzione UNION** selezionato in una **struttura SET** punta a una matrice di strutture che definiscono ogni membro di un set.

-   Set di valori

    Un set di valori viene usato quando Network Monitor includere un indicatore in-set o not-in-set con il valore trovato nel pacchetto del protocollo. Ad esempio, se viene specificato un set DWORD, Network Monitor visualizza un'etichetta per ogni valore DWORD trovato nel pacchetto del protocollo, a indicare che il valore DWORD è o non è specificato nel set.

    Un set di valori può essere basato sui tipi di dati BYTE, WORD, DWORD, LARGEINT e SYSTEMTIME.

-   Set di etichette

    Un set di etichette viene usato quando Network Monitor visualizzare un'etichetta definita dall'utente anziché i valori delle proprietà specificati in un set.

    Un set di etichette può essere basato su coppie di etichette BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME e BIT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[BIT CON \_ ETICHETTA](labeled-bit.md)
</dt> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




