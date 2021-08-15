---
description: Msival2.exe è un'utilità della riga di comando che può eseguire una suite di analizzatori di coerenza interna - ICE.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ed1228413d5b2fab0dfab79ea4546a9d15e74c8c62e9b1ca9751699f469854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943878"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe è un'utilità della riga di comando che può eseguire una suite di analizzatori di coerenza [interna - ICE.](internal-consistency-evaluators-ices.md)

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

Per altre informazioni sulle ICO e sul file CUB, vedere [Uso degli analizzatori di coerenza interna.](using-internal-consistency-evaluators.md)

## <a name="syntax"></a>Sintassi

**Msival2** *{database}{file CUB} \[ \] \[ -f -l {logfile} \] \[ -i {ICE Id} \[ :{ICE \] \] Id}...*

## <a name="command-line-options"></a>Opzioni da riga di comando

Msival2.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È anche possibile usare un delimitatore barra al posto di un trattino.



| Opzione | Descrizione                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtrare tutti i messaggi informativi dai risultati visualizzati. Vengono visualizzati tutti gli altri tipi di messaggi.                                                                                                                                                                                              |
| -i     | Eseguire solo le ICO elencate nella riga di comando nell'ordine specificato. Ogni azione personalizzata ICE deve essere elencata come visualizzata nella [tabella CustomAction](customaction-table.md) del file CUB. Se questa opzione viene omessa, lo strumento esegue il set predefinito di ICE specificato dall'autore del file CUB. |
| -l     | Scrive i risultati nel file specificato. Il file non deve esistere già. Se il file esiste, non viene sovrascritto.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



