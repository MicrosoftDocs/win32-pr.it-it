---
description: Intero collegato a una proprietà con i qualificatori BitMap e BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificatori BitMap e BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b02f2d9f2b6632d5f190d1537b2f33d822d916611983da71121ffbbded943d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051079"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Qualificatori BitMap e BitValue

Una bitmap è un intero collegato a una proprietà con i **qualificatori BitMap** e **BitValue.** Ogni bit del valore della proprietà funge da indice nella matrice di valori **nell'elenco BitValue.** Poiché più bit nel valore della proprietà possono essere "on" contemporaneamente, è possibile usare un singolo valore della proprietà per indicare più valori simultanei.

Ad esempio, l'esempio di codice MOF seguente stabilisce che la proprietà **FileType** contiene i qualificatori **BitMap** e **BitValues.** Stabilisce inoltre che il bit meno in ordine (bit 0) corrisponde al valore "Sola lettura". Il bit successivo (bit 1) corrisponde a "Hidden" e così via. Non tutti i bit devono essere significativi. In questo sistema a otto bit i due bit più significativi, 6 e 7, non hanno alcun significato.

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

Se la **proprietà FileType** segnala il valore 7 (bit 0000 0111), il file è "Read Only", "System" e "Hidden". Se la **proprietà FileType** segnala il valore 18 (0x12 bit 0001 0010), si tratta di una sottodirectory nascosta.

Esistono due tipi diversi di bitmap che usano il codice MOF:

-   Bit significativi consecutivi che iniziano con il bit meno significativo (bit 0)

    È possibile definire una matrice di valori di bit senza specificare in modo esplicito i bit significativi se i bit significativi iniziano con il bit meno significativo (bit 0) e avanzano verso l'alto senza interruzioni per tutti gli elementi nella matrice **BitValue.** Nell'esempio di codice MOF seguente viene eseguita la stessa funzione dell'esempio precedente.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Bit significativo preceduto da un bit non significativo

    Se il bit meno significativo è irrilevante o la sequenza di bit significativi non è continua, è necessario specificare entrambi i qualificatori **BitMap** e **BitValues.** Nell'esempio di codice MOF seguente viene illustrata una situazione in cui il bit meno significativo non è significativo e si verifica un gap nella sequenza di bit significativi.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    In questo caso, l'impostazione del bit meno significativo (bit 0) non ha alcun significato e viene ignorata. Tuttavia, l'impostazione del bit 1 (0x2) indica che questo messaggio di posta elettronica è contrassegnato per il follow-up, l'impostazione del bit 4 (0x8) indica che una conferma di recapito deve essere inviata al mittente quando il messaggio di posta elettronica è arrivato alla cassetta postale del destinatario e l'impostazione del bit 5 (0x10) specifica che una conferma di lettura deve essere inviata al mittente quando il messaggio di posta elettronica viene aperto dal destinatario. L'impostazione di tutti e tre i bit significativi (0x1A) specifica tutte e tre le condizioni per il messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Per decidere se usare i qualificatori / **BitMap BitValues** o **ValueMap** Values, determinare se uno dei valori indicati può /  verificarsi contemporaneamente. Se possono esistere più valori simultanei, è necessario usare **BitMap** / **BitValues**. Se tutti i valori si escludono a vicenda, è necessario usare i **qualificatori ValueMap** / **Values.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Qualificatori valueMap e value](value-map.md)
</dt> </dl>

 

 



