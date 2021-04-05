---
title: Oggetto configurazione del flusso
description: Oggetto configurazione del flusso
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, oggetti di configurazione di flusso
- ASF (Advanced Systems Format), oggetti di configurazione di flusso
- ASF (formato avanzato dei sistemi), oggetti di configurazione di flusso
- oggetti, flusso di oggetti di configurazione
- oggetti di configurazione di flusso
- flussi, oggetti di configurazione di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117458"
---
# <a name="stream-configuration-object"></a>Oggetto configurazione del flusso

Per specificare le proprietà di un flusso multimediale in un file ASF, viene usato un oggetto di configurazione del flusso. Gli oggetti di configurazione del flusso possono essere creati per i flussi esistenti in un profilo oppure possono essere creati vuoti, pronti per la ricezione di nuovi dati. Gli oggetti di configurazione del flusso non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di configurazione del flusso, è necessario chiamare [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) per aggiungere un nuovo flusso o [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per salvare le modifiche apportate a un flusso esistente.

Per creare un oggetto di configurazione del flusso, usare uno dei metodi seguenti.



| Metodo                                                                | Descrizione                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Crea un oggetto di configurazione del flusso senza dati.                                                                          |
| [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Crea un oggetto di configurazione del flusso popolato con i dati di un profilo. Usa l'indice del flusso per identificare il flusso desiderato.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Crea un oggetto di configurazione del flusso popolato con i dati di un profilo. Usa il numero di flusso per identificare il flusso desiderato. |



 

Tutti i metodi della tabella precedente impostano un puntatore a un'interfaccia **IWMStreamConfig** . Le altre interfacce dell'oggetto di configurazione del flusso possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto di configurazione del flusso.



| Interfaccia                                        | Descrizione                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Imposta e recupera la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Imposta e recupera le proprietà che non sono necessarie per tutti i flussi, ad esempio le impostazioni della velocità in bit (VBR) della variabile.                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Imposta e recupera tutte le informazioni di base su un flusso.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configura i tipi di estensioni di unità dati associate al flusso. Eredita tutti i metodi di **IWMStreamConfig**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Imposta e recupera la lingua per il flusso. Eredita tutti i metodi di **IWMStreamConfig** e **IWMStreamConfig2**. |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa ed è disponibile solo per i flussi video.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> </dl>

 

 




