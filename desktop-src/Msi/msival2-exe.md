---
description: Msival2.exe è un'utilità della riga di comando in grado di eseguire una suite di analizzatori di coerenza interni (CIEM).
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234035"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe è un'utilità della riga di comando in grado di eseguire una suite di [analizzatori di coerenza interni (CIEM](internal-consistency-evaluators-ices.md)).

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Per ulteriori informazioni su CIEM e il file CUB, vedere [utilizzo di analizzatori di coerenza interni](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Sintassi

**MSIVal2** *{database} {cub file} \[ -f \] \[ -l {logfile} \] \[ -i {ID ghiaccio} \[ : {Ice ID}... \] \]*

## <a name="command-line-options"></a>Opzioni da riga di comando

Msival2.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.



| Opzione | Descrizione                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtrare tutti i messaggi informativi dai risultati visualizzati. Vengono visualizzati tutti gli altri tipi di messaggi.                                                                                                                                                                                              |
| -i     | Eseguire solo i ghiacci elencati nella riga di comando nell'ordine specificato. Ogni azione personalizzata ICE dovrebbe essere elencata come appare nella [tabella CustomAction](customaction-table.md) del file cub. Se questa opzione viene omessa, lo strumento esegue il set predefinito di file di base (CIEM) specificato dall'autore del file CUB. |
| -l     | Scrive i risultati nel file specificato. Il file non deve essere già esistente. Se il file esiste, non verrà sovrascritto.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



