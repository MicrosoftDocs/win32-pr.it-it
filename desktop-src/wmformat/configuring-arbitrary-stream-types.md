---
title: Configurazione di tipi di flusso arbitrari
description: Configurazione di tipi di flusso arbitrari
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flussi, configurazione di tipi di flusso arbitrari
- codec, configurazione di tipi di flusso arbitrari
- flussi, GenProfile
- codec, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298215"
---
# <a name="configuring-arbitrary-stream-types"></a>Configurazione di tipi di flusso arbitrari

Per la maggior parte dei tipi di flusso arbitrario è sufficiente una velocità in bit, una finestra del buffer e un tipo di supporto principale appropriato nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Tuttavia, alcuni tipi arbitrari richiedono una configurazione aggiuntiva.

Se si riscontrano problemi durante la configurazione di un flusso, vedere l'applicazione di esempio denominata GenProfile, inclusa in questo SDK. La libreria definita in GenProfile contiene il codice per includere tutti i tipi di flussi. Per ulteriori informazioni su GenProfile e sugli altri esempi, vedere [applicazioni di esempio](sample-applications.md).

Nelle sezioni seguenti viene descritto come configurare i tipi di flusso arbitrari.



| Sezione                                                                                                                                        | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configurazione di flussi di script](configuring-script-streams.md)                                                                                   | Viene descritto come configurare i flussi di script.                                                  |
| [Configurazione di flussi di trasferimento di file](configuring-file-transfer-streams.md)                                                                     | Viene descritto come configurare i flussi di trasferimento di file.                                           |
| [Configurazione di flussi Web](configuring-web-streams.md)                                                                                         | Viene descritto come configurare i flussi Web.                                                     |
| [Configurazione di flussi di testo](configuring-text-streams.md)                                                                                       | Viene descritto come configurare i flussi di testo.                                                    |
| [Configurazione di flussi arbitrari personalizzati](configuring-custom-arbitrary-streams.md)                                                               | Viene descritto come configurare i flussi per i tipi di flusso arbitrari personalizzato.                       |
| [Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Viene descritto come calcolare la velocità in bit e le impostazioni della finestra del buffer per un flusso arbitrario. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi arbitrari**](arbitrary-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




