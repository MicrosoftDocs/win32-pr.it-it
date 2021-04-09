---
description: Una directory che contiene una o più directory è l'elemento padre della directory o directory contenuta e ogni directory indipendente è un elemento figlio della directory padre. La struttura gerarchica delle directory viene definita albero di directory.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informazioni sulla gestione delle directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879302"
---
# <a name="about-directory-management"></a>Informazioni sulla gestione delle directory

Una directory che contiene una o più directory è l' *elemento padre* della directory o directory contenuta e ogni directory indipendente è un elemento *figlio* della directory padre. La struttura gerarchica delle directory viene definita *albero di directory*.

Il file system NTFS implementa il collegamento logico tra una directory e i file in esso contenuti come *tabella voce di directory*. Quando un file viene spostato in una directory, viene creata una voce nella tabella per il file spostato e il nome del file viene inserito nella voce. Quando un file contenuto in una directory viene eliminato, anche il nome e la voce corrispondenti al file eliminato vengono eliminati dalla tabella. In una tabella di voci di directory possono esistere più voci per un singolo file. Se nella tabella viene creata una voce aggiuntiva per un file, tale voce viene definita *collegamento* reale a tale file. Non esiste alcun limite al numero di collegamenti reali che è possibile creare per un singolo file.

Le directory possono inoltre contenere giunzioni e reparse point.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                 | Descrizione                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Creazione ed eliminazione di directory](creating-and-deleting-directories.md)<br/> | Un'applicazione può creare ed eliminare le directory a livello di codice.<br/>                          |
| [Handle di directory](obtaining-a-handle-to-a-directory.md)<br/>                 | Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.<br/> |
| [Punti di analisi](reparse-points.md)<br/>                                       | Descrive i reparse point.<br/>                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla gestione delle directory](directory-management-reference.md)
</dt> </dl>

 

 




