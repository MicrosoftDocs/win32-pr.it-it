---
title: Oggetto configurazione del flusso
description: Oggetto configurazione del flusso
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, oggetti di configurazione del flusso
- Advanced Systems Format (ASF), oggetti di configurazione del flusso
- ASF (Advanced Systems Format), oggetti di configurazione di flusso
- oggetti, oggetti di configurazione del flusso
- oggetti di configurazione del flusso
- flussi, oggetti di configurazione del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e71be6149df3f2da0edba31d9c5803d86a6fd89189e1fc339cf99593336415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929381"
---
# <a name="stream-configuration-object"></a>Oggetto configurazione del flusso

Un oggetto di configurazione del flusso viene usato per specificare le proprietà di un flusso multimediale in un file ASF. Gli oggetti di configurazione del flusso possono essere creati per i flussi esistenti in un profilo o possono essere creati vuoti, pronti per ricevere nuovi dati. Gli oggetti di configurazione del flusso non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di configurazione del flusso, è necessario chiamare [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) per aggiungere un nuovo flusso o [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per salvare le modifiche apportate a un flusso esistente.

Per creare un oggetto di configurazione del flusso, usare uno dei metodi seguenti.



| Metodo                                                                | Descrizione                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Crea un oggetto di configurazione del flusso senza dati.                                                                          |
| [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Crea un oggetto di configurazione del flusso popolato con i dati di un profilo. Usa l'indice del flusso per identificare il flusso desiderato.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Crea un oggetto di configurazione del flusso popolato con i dati di un profilo. Usa il numero di flusso per identificare il flusso desiderato. |



 

Tutti i metodi nella tabella precedente impostano un puntatore a **un'interfaccia IWMStreamConfig.** Le altre interfacce dell'oggetto di configurazione del flusso possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto di configurazione del flusso.



| Interfaccia                                        | Descrizione                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Imposta e recupera la struttura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Imposta e recupera le proprietà non necessarie per tutti i flussi, ad esempio le impostazioni vbr (Variable Bit Rate).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Imposta e recupera tutte le informazioni di base su un flusso.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configura i tipi di estensioni unità dati associate al flusso. Eredita tutti i metodi di **IWMStreamConfig.** |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Imposta e recupera la lingua per il flusso. Eredita tutti i metodi di **IWMStreamConfig** e **IWMStreamConfig2.** |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa ed è disponibile solo per i flussi video.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> </dl>

 

 




