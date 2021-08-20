---
title: Configurazione di tipi di flusso arbitrari
description: Configurazione di tipi di flusso arbitrari
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flussi, configurazione di tipi di flusso arbitrari
- codec, configurazione di tipi di flusso arbitrari
- flussi, GenProfile
- codecs,GenProfile
- Profilo gen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260219e408872dc21ecf82bd64b59b6c12b014c6e073a687a1b55957b290b76f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548050"
---
# <a name="configuring-arbitrary-stream-types"></a>Configurazione di tipi di flusso arbitrari

La maggior parte dei tipi di flusso arbitrari ha bisogno solo di una velocità in bit, di una finestra del buffer e di un tipo di supporto principale appropriato nella [**struttura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Tuttavia, alcuni tipi arbitrari richiedono una configurazione aggiuntiva.

In caso di problemi di configurazione di un flusso, vedere l'applicazione di esempio denominata GenProfile, inclusa in questo SDK. La libreria definita in GenProfile contiene il codice per includere tutti i tipi di flussi. Per altre informazioni su GenProfile e gli altri esempi, vedere [Applicazioni di esempio.](sample-applications.md)

Le sezioni seguenti descrivono come configurare tipi di flusso arbitrari.



| Sezione                                                                                                                                        | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configurazione degli script Flussi](configuring-script-streams.md)                                                                                   | Viene descritto come configurare i flussi di script.                                                  |
| [Configurazione del trasferimento di file Flussi](configuring-file-transfer-streams.md)                                                                     | Viene descritto come configurare i flussi di trasferimento file.                                           |
| [Configurazione dell'Flussi Web](configuring-web-streams.md)                                                                                         | Viene descritto come configurare i flussi Web.                                                     |
| [Configurazione dell'Flussi](configuring-text-streams.md)                                                                                       | Viene descritto come configurare i flussi di testo.                                                    |
| [Configurazione di regole arbitrarie Flussi](configuring-custom-arbitrary-streams.md)                                                               | Viene descritto come configurare flussi per tipi di flusso arbitrari personalizzati.                       |
| [Calcolo della frequenza di bit e dei valori della finestra del buffer per le Flussi](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Viene descritto come calcolare la velocità in bit e le impostazioni della finestra del buffer per un flusso arbitrario. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Codice Flussi**](arbitrary-streams.md)
</dt> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> </dl>

 

 




