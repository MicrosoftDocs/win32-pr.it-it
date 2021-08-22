---
description: ICE18 verifica che tutte le directory vuote usate come percorso della chiave per un componente siano elencate nella tabella CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca102e8fdec5e30283cd879ddb5677a2bba79f90ba5a9a790ea50923e0aeedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581141"
---
# <a name="ice18"></a>ICE18

ICE18 verifica che tutte le directory vuote usate come percorso di chiave per un componente siano elencate nella [tabella CreateFolder](createfolder-table.md).

Se la colonna KeyPath della [tabella Component](component-table.md) è Null, significa che la directory elencata nella colonna Directory è \_ il percorso chiave per il componente. Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, questa cartella deve essere elencata nella tabella [CreateFolder](createfolder-table.md) per evitare che il programma di installazione tenti di installarlo ogni volta.

Non impostare la directory SystemFolder come percorso della chiave di un componente. Poiché questa cartella è presente in ogni sistema operativo, il programma di installazione rileva sempre il percorso della chiave indipendentemente dal fatto che il componente sia o meno presente. In questo caso, il percorso della chiave deve essere un file, una voce del Registro di sistema o un'origine dati ODBC.

Quando si esegue una convalida ICE18 verifica innanzitutto se le condizioni seguenti sono tutte vere:

-   La colonna KeyPath della [tabella Component contiene](component-table.md) un valore Null.
-   Nessun file elencato per il componente nella [tabella File](file-table.md).
-   Nessun file per il componente elencato nella tabella [RemoveFile](removefile-table.md) e che il valore in DirProperty corrisponde alla colonna Directory della \_ [tabella Component](component-table.md).
-   Nessun file per il componente elencato nella tabella [DuplicateFile](duplicatefile-table.md) e che il valore in DestFolder corrisponde alla colonna Directory della \_ [tabella Component](component-table.md).
-   Nessun file per il componente elencato nella tabella [MoveFile](movefile-table.md) e che il valore in DestFolder corrisponde alla colonna Directory della \_ [tabella Component](component-table.md).

Se sono tutte vere, ICE18 convalida quanto segue:

-   Che la colonna \_ Component della [tabella CreateFolder](createfolder-table.md) abbia lo stesso valore della colonna Component della [tabella Component](component-table.md).
-   Che la colonna Directory della tabella CreateFolder abbia lo stesso valore della \_ colonna Directory della tabella \_ [Component](component-table.md).

## <a name="result"></a>Risultato

ICE18 invia un messaggio di errore se il pacchetto di installazione specifica una directory come percorso della chiave per il componente non elencato nella [tabella CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



