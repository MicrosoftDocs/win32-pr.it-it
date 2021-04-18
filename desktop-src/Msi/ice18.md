---
description: ICE18 verifica che tutte le directory vuote utilizzate come percorso della chiave per un componente siano elencate nella tabella CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308192"
---
# <a name="ice18"></a>ICE18

ICE18 verifica che tutte le directory vuote utilizzate come percorso della chiave per un componente siano elencate nella [tabella CreateFolder](createfolder-table.md).

Se la colonna del percorso di chiave della [tabella dei componenti](component-table.md) è null, significa che la directory elencata nella colonna directory \_ è il percorso della chiave per tale componente. Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, la cartella deve essere elencata nella [tabella CreateFolder](createfolder-table.md) per impedire che il programma di installazione tenti di installare ogni volta.

Non rendere la directory SystemFolder il percorso della chiave di un componente. Poiché questa cartella è presente in ogni sistema operativo, il programma di installazione rileva sempre il percorso della chiave, indipendentemente dal fatto che il componente sia presente o meno. In questo caso, il percorso della chiave deve essere un file, una voce del registro di sistema o un'origine dati ODBC.

Quando si esegue un ICE18 di convalida, verifica innanzitutto se sono soddisfatte le condizioni seguenti:

-   La colonna di percorso della [tabella dei componenti](component-table.md) contiene un valore null.
-   Non sono presenti file elencati per il componente nella [tabella file](file-table.md).
-   Che non siano presenti file per il componente elencati nella [tabella RemoveFile](removefile-table.md) e che il valore in DirProperty corrisponda alla \_ colonna directory della [tabella Component](component-table.md).
-   Che non siano presenti file per il componente elencati nella [tabella DuplicateFile](duplicatefile-table.md) e che il valore in DestFolder corrisponda alla \_ colonna directory della [tabella Component](component-table.md).
-   Che non siano presenti file per il componente elencati nella [tabella MoveFile](movefile-table.md) e che il valore in DestFolder corrisponda alla \_ colonna directory della [tabella Component](component-table.md).

Se si verificano tutte le condizioni, ICE18 convalida quanto segue:

-   Il valore della \_ colonna Component della [tabella CreateFolder](createfolder-table.md) è uguale a quello della colonna Component della [tabella Component](component-table.md).
-   Il valore della \_ colonna directory della tabella CreateFolder è uguale a quello della colonna directory \_ della [tabella Component](component-table.md).

## <a name="result"></a>Risultato

ICE18 Invia un messaggio di errore se il pacchetto di installazione specifica una directory come percorso della chiave per il componente che non è elencato nella [tabella CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



