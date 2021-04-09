---
title: Oggetto profilo
description: Oggetto profilo
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media Format SDK, oggetti profilo
- ASF (Advanced Systems Format), oggetti profilo
- ASF (formato avanzato dei sistemi), oggetti profilo
- oggetti, profili
- profili, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858081"
---
# <a name="profile-object"></a>Oggetto profilo

Un oggetto profilo gestisce le impostazioni di un profilo. Gli oggetti profilo possono essere creati per i dati di profilo esistenti oppure possono essere creati vuoti, pronti per la ricezione di nuovi dati. Un oggetto profilo viene inoltre creato dall'oggetto Reader (e dall'oggetto Reader sincrono) quando un file viene caricato per la lettura. In questo caso l'oggetto viene popolato con le informazioni sul profilo archiviate nell'intestazione del file.

Per salvare il contenuto di un oggetto profilo, è necessario chiamare [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).

Un profilo contiene più oggetti che controllano vari aspetti del profilo, ad esempio i flussi. Tutti questi oggetti sono subordinati all'oggetto profilo. Questi oggetti non vengono creati con le funzioni di creazione come si farebbe con gli oggetti principali di questo SDK. Al contrario, le interfacce dell'oggetto profilo contengono metodi che creano gli oggetti subordinati.

Per creare un oggetto profilo, chiamare uno dei metodi seguenti.



| Metodo                                                                                | Descrizione                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | Crea un oggetto profilo senza dati del profilo.                                                                                                              |
| [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | Crea un oggetto profilo popolato con i dati di un profilo salvato sotto forma di stringa. Questo è l'unico modo per creare un oggetto profilo con i dati di un profilo personalizzato. |
| [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | Crea un oggetto profilo popolato con i dati di un profilo di sistema. Usa il GUID per identificare il profilo di sistema desiderato.                                       |
| [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | Crea un oggetto profilo popolato con i dati di un profilo di sistema. Usa l'indice del profilo per identificare il profilo di sistema desiderato.                              |



 

Tutti i metodi della tabella precedente impostano un puntatore a un'interfaccia **IWMProfile** . Le altre interfacce dell'oggetto profilo possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate da ogni oggetto profilo.



| Interfaccia                                  | Descrizione                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | Gestisce un elenco di lingue supportate da un file ASF.                                                                                             |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | Controlla la dimensione massima dei pacchetti in un file.                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | Controlla la dimensione minima dei pacchetti in un file. Eredita tutti i metodi di **IWMPacketSize**.                                                 |
| [**IWMProfile**](iwmprofile.md)           | Controlla le impostazioni di base e gli oggetti inclusi in un profilo.                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | Recupera l'identificatore univoco globale (GUID) associato al profilo. Eredita tutti i metodi di **IWMProfile**.                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | Controlla la condivisione della larghezza di banda e le informazioni relative alla priorità del flusso in un profilo. Eredita tutti i metodi di **IWMProfile** e **IWMProfile2**. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> <dt>

[**Profili**](profiles.md)
</dt> </dl>

 

 




