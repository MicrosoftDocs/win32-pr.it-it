---
description: Una directory che contiene una o più directory è l'elemento padre della directory o delle directory contenute e ogni directory contenuta è un elemento figlio della directory padre. La struttura gerarchica delle directory viene definita albero di directory.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informazioni sulla gestione delle directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cc59e465e1d97b28b1cfdff35c5f288e56b5eb0ee9800273873ffe6476868b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766411"
---
# <a name="about-directory-management"></a>Informazioni sulla gestione delle directory

Una directory che contiene una  o più directory è l'elemento padre della directory o delle directory contenute e ogni directory contenuta è un elemento *figlio* della directory padre. La struttura gerarchica delle directory viene definita albero *di directory*.

Il file system NTFS implementa il collegamento logico tra una directory e i file in essa contenuti come tabella *di voci di directory*. Quando un file viene spostato in una directory, viene creata una voce nella tabella per il file spostato e il nome del file viene inserito nella voce. Quando viene eliminato un file contenuto in una directory, dalla tabella vengono eliminati anche il nome e la voce corrispondenti al file eliminato. In una tabella di voci di directory possono esistere più voci per un singolo file. Se viene creata una voce aggiuntiva nella tabella per un file, tale voce viene definita collegamento *rigido* a tale file. Non esiste alcun limite al numero di collegamenti rigidi che è possibile creare per un singolo file.

Le directory possono anche contenere giunzioni e reparse point.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                 | Descrizione                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Creazione ed eliminazione di directory](creating-and-deleting-directories.md)<br/> | Un'applicazione può creare ed eliminare directory a livello di codice.<br/>                          |
| [Handle di directory](obtaining-a-handle-to-a-directory.md)<br/>                 | Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.<br/> |
| [Punti di analisi](reparse-points.md)<br/>                                       | Descrive i reparse point.<br/>                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla gestione della directory](directory-management-reference.md)
</dt> </dl>

 

 




