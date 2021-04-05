---
title: Estensioni unità dati
description: Estensioni unità dati
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, estensioni di unità dati
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- Windows Media Format SDK, sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- estensioni unità dati, informazioni
- estensioni unità di payload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723495"
---
# <a name="data-unit-extensions"></a>Estensioni unità dati

Windows Media Format SDK consente di integrare i dati negli esempi con le *estensioni di unità dati*, denominate anche sistemi di estensione del payload. Questa documentazione usa il termine "estensioni dell'unità dati" per mantenere la coerenza con i nomi dei metodi, ad esempio [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension). Un'estensione dell'unità dati è una coppia nome/valore collegata all'esempio nella sezione dati del file. È possibile accedere ai dati estesi utilizzando i metodi dell'oggetto buffer quando l'esempio viene recuperato dal reader.

È possibile creare estensioni di unità dati per le specifiche, ma molti tipi sono predefiniti e supportati dagli oggetti di questo SDK. Queste estensioni standard vengono usate per fornire dati aggiuntivi per i nomi di file (nei flussi di script e Web), i dati del codice in tempo SMPTE, le proporzioni dei pixel non quadrati, la durata e il tipo di interlacciamento.

Per usare le estensioni dell'unità dati, è necessario configurare il flusso per accettarle e quindi aggiungere estensioni a ogni esempio per il flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Impostazione delle estensioni delle unità dati**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




