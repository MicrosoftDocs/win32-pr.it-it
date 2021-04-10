---
title: File di codice per l'esempio di provider di origine
description: File di codice per l'esempio di provider di origine
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- Windows Media Gestione dispositivi, esempio di provider di servizi
- Gestione dispositivi, esempio di provider di servizi
- provider di servizi, esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116841"
---
# <a name="code-files-for-the-source-provider-sample"></a>File di codice per l'esempio di provider di origine

Il progetto del provider di origine di esempio include i file di codice sorgente seguenti, con le intestazioni associate:



| File                   | Descrizione                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch. cpp            | Include file ATL standard.                                                                                                                                                                                    |
| chiave. c                  | Contiene una chiave di autenticazione fittizia.                                                                                                                                                                            |
| loghelp. cpp            | Contiene funzioni che registrano l'attività e gli errori usando la classe **WMDMLogger** , implementata nel file di sistema WMDMLOG.dll.                                                                         |
| MDServiceProvider. cpp  | Implementa una classe, CMDServiceProvider, che implementa le interfacce [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.                                                             |
| MDSP. cpp               | Il codice di registrazione e il punto di ingresso della DLL.                                                                                                                                                                          |
| MDSPDevice. cpp         | Implementa una classe, CMDSPDevice, che implementa le interfacce [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages** .                          |
| MDSPEnumDevice. cpp     | Implementa una classe, CMDSPEnumDevice, che implementa l'interfaccia [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .                                                                                                  |
| MDSPEnumStorage. cpp    | Implementa una classe, CMDSPEnumStorage, che implementa l'interfaccia [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .                                                                                               |
| MDSPStorage. cpp        | Implementa una classe, CMDSPStorage, che implementa le interfacce [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .                    |
| MDSPStorageGlobals. cpp | Implementa una classe, CMDSPStorageGlobals, che implementa l'interfaccia [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .                                                                                      |
| MDSPutil. cpp           | Contiene varie funzioni di utilità per la gestione dei dispositivi e dei file.                                                                                                                                              |
| pagina di appoggio. cpp           | Implementa una classe, CPropPage, che eredita le classi ATL **IPropertyPageImpl** (per implementare IPropertyPage) e **CDialogImpl**, che eredita la classe ATL CDialogImpl (per gestire Windows e i messaggi). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Provider di servizi di esempio**](sample-service-provider.md)
</dt> </dl>

 

 




