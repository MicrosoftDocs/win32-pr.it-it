---
title: File di codice per l'esempio di provider di origine
description: File di codice per l'esempio di provider di origine
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- Windows Media Device Manager, esempio di provider di servizi
- Device Manager, esempio di provider di servizi
- provider di servizi, esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c29127aebea6898868b29adb17a15c8d174e1fedfd3228bd565bf8ef4ce9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586368"
---
# <a name="code-files-for-the-source-provider-sample"></a>File di codice per l'esempio di provider di origine

Il progetto del provider di origine di esempio include i file di codice sorgente seguenti, con intestazioni associate:



| File                   | Descrizione                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch.cpp            | Include file ATL standard.                                                                                                                                                                                    |
| key.c                  | Contiene una chiave di autenticazione fittizia.                                                                                                                                                                            |
| loghelp.cpp            | Contiene funzioni che registrano attività ed errori usando la classe **WMDMLogger,** implementata nel file WMDMLOG.dll di sistema.                                                                         |
| MDServiceProvider.cpp  | Implementa una classe, CMDServiceProvider, che implementa le [**interfacce IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.                                                             |
| mdsp.cpp               | Punto di ingresso DLL e codice di registrazione.                                                                                                                                                                          |
| MDSPDevice.cpp         | Implementa una classe, CMDSPDevice, che implementa le [**interfacce IMDSPDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2) [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages.**                          |
| MDSPEnumDevice.cpp     | Implementa una classe, CMDSPEnumDevice, che implementa [**l'interfaccia IMDSPEnumDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)                                                                                                  |
| MDSPEnumStorage.cpp    | Implementa una classe, CMDSPEnumStorage, che implementa [**l'interfaccia IMDSPEnumStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)                                                                                               |
| MDSPStorage.cpp        | Implementa una classe, CMDSPStorage, che implementa le [**interfacce IMDSPStorage2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2) [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                    |
| MDSPStorageGlobals.cpp | Implementa una classe, CMDSPStorageGlobals, che implementa [**l'interfaccia IMDSPStorageGlobals.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)                                                                                      |
| MDSPutil.cpp           | Contiene varie funzioni di utilità per la gestione di dispositivi e file.                                                                                                                                              |
| proppage.cpp           | Implementa una classe, CPropPage, che eredita le classi ATL **IPropertyPageImpl** (per implementare IPropertyPage) e **CDialogImpl**, che eredita la classe ATL CDialogImpl (per gestire finestre e messaggi). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Provider di servizi di esempio**](sample-service-provider.md)
</dt> </dl>

 

 




