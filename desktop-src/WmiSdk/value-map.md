---
description: Una mappa di valori è una matrice collegata a una proprietà con il valore e i qualificatori ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Qualificatori ValueMap e value
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315184"
---
# <a name="valuemap-and-value-qualifiers"></a>Qualificatori ValueMap e value

Una mappa di valori è una matrice collegata a una proprietà con il **valore** e i qualificatori **ValueMap** .

La proprietà funge da indice nella matrice, mantenendo un valore che rappresenta uno dei valori nella matrice. Utilizzando il codice MOF, è possibile disporre dei seguenti tipi di mappe dei valori:

-   Mapping della matrice a un intero.

    È possibile definire una matrice con il qualificatore del **valore** e collegare la matrice direttamente a una proprietà Integer, come illustrato nell'esempio seguente:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    In questo esempio il valore della proprietà **status** è un indice nella matrice di stringhe definita per **valore**. La proprietà può assumere solo valori che corrispondono alle posizioni ordinali nella matrice di **valori** meno 1. Ad esempio, se si imposta **status** su "1" viene eseguito il mapping al valore "Error". La proprietà index può assumere solo valori che corrispondono alle posizioni nella matrice di **valori** . Se, ad esempio, la matrice contiene 10 voci, la proprietà index può essere storia da 0 a 9, non 30 o 177.

-   Mapping della matrice a un altro mapping della matrice a un intero.

    Se si desidera creare un indice che non utilizza un sistema ordinale di conteggio, utilizzare il qualificatore **ValueMap** . Il qualificatore **ValueMap** configura un'altra matrice che contiene un sistema di numerazione degli indici arbitrari, come illustrato nell'esempio seguente:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Sebbene sia necessario inserire i valori di **ValueMap** in Quotations, WMI considera i valori integer. Pertanto, in questo esempio è possibile impostare la proprietà **status** su un valore integer nel set di **ValueMap** : 1, 3, 99 o 0. WMI esegue il mapping di ogni intero da una posizione ordinale nella matrice di stringhe **ValueMap** a una posizione corrispondente nella matrice di **valori** . Ad esempio, l'impostazione **dello stato** su 0 corrisponde a "Unknown".

-   Mapping della matrice a un altro mapping della matrice a una stringa.

    Se non si vuole usare un numero intero per indicizzare la matrice, è possibile usare invece una stringa per includere uno dei valori possibili nella matrice. A tale scopo, è necessario definire sia un **valore** sia una matrice **ValueMap** che contengono entrambe stringhe, come illustrato nell'esempio seguente:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Con una proprietà stringa, i valori effettivi consentiti della proprietà sono le voci nella matrice **ValueMap** . Ad esempio, è possibile impostare **lo stato** su "OK" o "sconosciuto".

L'applicazione può sfruttare i vantaggi dei mapping in modo utile. Il provider deve applicare un intervallo di valori valido.

## <a name="remarks"></a>Commenti

Per decidere se utilizzare il valore **ValueMap** /  o i  / qualificatori di bitmap **BitValues** , determinare se uno dei valori indicati potrebbe verificarsi simultaneamente. Se possono esistere più valori simultanei, è necessario utilizzare la **bitmap** / **BitValues**. Se tutti i valori si escludono a vicenda, è necessario usare i / qualificatori di **valore** ValueMap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[BitMap e BitValue](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



