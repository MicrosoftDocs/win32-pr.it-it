---
description: Dopo aver selezionato gli ICO appropriati per la convalida, uno sviluppatore deve raccogliere le azioni personalizzate insieme in un database ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creazione di un database ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e078517f8942454320e3f743d7379bbfeb22a7c44afe635a8276568a56c27f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926991"
---
# <a name="building-an-ice-database"></a>Creazione di un database ICE

Dopo aver selezionato gli [ICO appropriati per](internal-consistency-evaluators-ices.md) la convalida, uno sviluppatore deve raccogliere le azioni personalizzate insieme in un database ICE. Un file con estensione cub è un database .msi standard che contiene solo ICE e le relative tabelle necessarie. Non è possibile installare un file con estensione cub e viene usato solo per archiviare e fornire l'accesso alle azioni personalizzate ICE.

Un file con estensione cub contiene le tabelle di database seguenti.



| Tabella                                  | Descrizione                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binario](binary-table.md)             | File di script, DLL ed exE delle azioni ice actions a cui viene fatto riferimento nella tabella CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Ogni record in questa tabella corrisponde a un'azione personalizzata ICE inclusa nel file con estensione cub.                                                                                                                                                                                   |
| \_ICESequence                          | In questa tabella sono elencate le azioni di condivisione ICE incluse nel file con estensione cub nella sequenza di esecuzione. Le azioni personalizzate ICE elencate in questa tabella vengono eseguite chiamando [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)o singolarmente usando [**MsiDoAction.**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) |
| [\_Convalida](-validation-table.md)  | Questa tabella contiene le voci del file con estensione cub che devono essere unite nella \_ tabella Validation.                                                                                                                                                                               |
| \_Speciale                              | Eventuali tabelle di elaborazione speciali richieste da particolari azioni personalizzate ICE devono essere incluse nel file con estensione cub. Il nome di queste tabelle deve contenere un carattere di sottolineatura iniziale.                                                                                                        |



 

Vedere [File con estensione cub di esempio.](sample--cub-file.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un ice](building-an-ice.md)
</dt> </dl>

 

 



