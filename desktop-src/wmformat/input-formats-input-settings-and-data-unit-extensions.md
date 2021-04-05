---
title: Formati di input, impostazioni di input ed estensioni di unità dati
description: Formati di input, impostazioni di input ed estensioni di unità dati
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media Format SDK, formati di input e impostazioni
- Windows Media Format SDK, estensioni di unità dati
- Windows Media Format SDK, sistemi di estensione del payload
- ASF (Advanced Systems Format), formati e impostazioni di input
- ASF (formato avanzato dei sistemi), formati e impostazioni di input
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- ASF (Advanced Systems Format), sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- estensioni unità dati, informazioni
- sistemi di estensione del payload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955713"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a>Formati di input, impostazioni di input ed estensioni di unità dati

L'oggetto Writer supporta le impostazioni di input, i formati di input e le estensioni dell'unità dati, che consentono di controllare le funzionalità del writer. Non è sempre ovvio quali metodi utilizzare per controllare una funzionalità specifica.

I formati di input sono formati multimediali che descrivono le proprietà di base del supporto passato al writer per la codifica. Ad esempio, le dimensioni del frame e lo spazio colore del video di input sono descritti dal formato di input.

Le impostazioni di input sono caratteristiche dei dati di input oltre le nozioni di base o informazioni sulle trasformazioni da eseguire sui dati. Le impostazioni video interlacciate e le informazioni su un sistema di filigrana sono esempi di impostazioni di input.

Le estensioni dell'unità dati, denominate anche sistemi di estensione del payload, sono valori collegati a singoli campioni nella sezione dati del file. I codici temporali SMPTE e le informazioni sui pixel non quadrati sono esempi di estensioni di unità dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Estensioni unità dati**](data-unit-extensions.md)
</dt> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Enumerazione del formato di input**](input-format-enumeration.md)
</dt> <dt>

[**Impostazioni di input**](input-settings.md)
</dt> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> </dl>

 

 




