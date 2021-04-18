---
description: È un numero intero collegato a una proprietà con i qualificatori di BitMap e BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificatori BitMap e BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310415"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Qualificatori BitMap e BitValue

Una bitmap è un numero intero collegato a una proprietà con i qualificatori di **bitmap** e **BitValue** . Ogni bit del valore della proprietà funge da indice nella matrice di valori nell'elenco di **BitValue** . Poiché più bit nel valore della proprietà possono essere contemporaneamente "on", è possibile usare un singolo valore di proprietà per indicare più valori simultanei.

Ad esempio, l'esempio di codice MOF seguente stabilisce la proprietà **FileType** con i qualificatori **bitmap** e **BitValues** . Stabilisce inoltre che il bit di ordine inferiore (bit 0) corrisponde al valore di "sola lettura". Il bit successivo (bit 1) corrisponde a "hidden" e così via. (Non tutti i bit devono essere significativi. In questo sistema a otto bit, i due bit di ordine superiore, 6 e 7, non hanno alcun significato.

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

Se la proprietà **FileType** riporta il valore 7 (BITS 0000 0111), il file è di sola lettura, "System" e "hidden". Se la proprietà **FileType** riporta il valore 18 (0x12, BITS 0001 0010), si tratta di una sottodirectory nascosta.

Esistono due tipi diversi di bitmap che usano il codice MOF:

-   Bit significativi consecutivi che iniziano con il bit di ordine inferiore (bit 0)

    È possibile definire una matrice di valori di bit senza specificare in modo esplicito i bit significativi se i bit significativi iniziano con il bit di ordine inferiore (bit 0) e avanzare verso l'alto senza interruzioni in tutti gli elementi della matrice **BitValue** . Nell'esempio di codice MOF seguente viene eseguita la stessa funzione dell'esempio precedente.

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

    Se il bit di ordine inferiore non è significativo o la sequenza di bit significativi non è continua, è necessario specificare sia la **bitmap** che i qualificatori **BitValues** . Nell'esempio di codice MOF riportato di seguito viene illustrata una situazione in cui il bit di ordine inferiore non è significativo e si verifica un gap nella sequenza di bit significativi.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    In questo caso, l'impostazione del bit di ordine inferiore (bit 0) non ha significato e viene ignorata. Tuttavia, l'impostazione del bit 1 (0x2) indica che questo messaggio di posta elettronica è contrassegnato per il completamento, l'impostazione del bit 4 (0x8) indica che una ricevuta di recapito deve essere inviata al mittente quando il messaggio di posta elettronica è arrivato alla cassetta postale del destinatario e l'impostazione del bit 5 (0x10) specifica che una ricevuta di lettura deve essere inviata al mittente quando il messaggio di Impostando tutti e tre i bit significativi (0x1A) si specificano tutte e tre le condizioni per il messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Per decidere se utilizzare i qualificatori dei valori di **bitmap** / **BitValues** o **ValueMap** /  , determinare se i valori indicati possono verificarsi simultaneamente. Se possono esistere più valori simultanei, è necessario utilizzare la **bitmap** / **BitValues**. Se tutti i valori si escludono a vicenda, è necessario usare i / qualificatori dei **valori** ValueMap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Qualificatori ValueMap e value](value-map.md)
</dt> </dl>

 

 



