---
description: Dopo aver selezionato il CIEM appropriato per la convalida, lo sviluppatore deve raccogliere le azioni personalizzate in un database ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creazione di un database di ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881070"
---
# <a name="building-an-ice-database"></a>Creazione di un database di ghiaccio

Dopo aver selezionato il [CIEM](internal-consistency-evaluators-ices.md) appropriato per la convalida, lo sviluppatore deve raccogliere le azioni personalizzate in un database Ice. Un file con estensione cub è un database standard con estensione msi che contiene solo i ghiacci e le tabelle necessarie. Non è possibile installare un file con estensione cub e viene usato solo per archiviare e fornire l'accesso alle azioni personalizzate di ICE.

Un file con estensione cub contiene le tabelle di database seguenti.



| Tabella                                  | Descrizione                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binario](binary-table.md)             | I file di script, le dll e i file exe delle azioni doganali del ghiaccio a cui viene fatto riferimento nella tabella CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Ogni record di questa tabella corrisponde a un'azione personalizzata ICE inclusa nel file con estensione cub.                                                                                                                                                                                   |
| \_ICESequence                          | Questa tabella elenca le azioni doganali del ghiaccio incluse nel file con estensione cub nella sequenza di esecuzione. Le azioni personalizzate ICE elencate in questa tabella vengono eseguite chiamando [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)oppure eseguite singolarmente mediante [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). |
| [\_Convalida](-validation-table.md)  | Questa tabella contiene le voci di file con estensione cub da unire nella tabella di \_ convalida.                                                                                                                                                                               |
| \_Speciali                              | Tutte le tabelle di elaborazione speciali richieste da particolari azioni personalizzate del ghiaccio devono essere incluse nel file con estensione cub. Il nome di queste tabelle deve avere un carattere di sottolineatura principale.                                                                                                        |



 

Vedere il [file Sample. cub](sample--cub-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un ghiaccio](building-an-ice.md)
</dt> </dl>

 

 



