---
title: Compilazione dei file IDL forniti con l'SDK
description: Compilazione dei file IDL forniti con l'SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Gestione dispositivi Windows Media, file IDL
- Gestione dispositivi, file IDL
- applicazioni desktop, file IDL
- provider di servizi, file IDL
- guida per programmatori,file IDL
- IDL (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444012"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilazione dei file IDL forniti con l'SDK

Windows Media Device Manager SDK include sia i file di intestazione che i file IDL di origine per la maggior parte di questi file di intestazione. I file di intestazione si trovano nella cartella \\ inc nel percorso di installazione \\ dell'SDK. I file IDL si trovano nella \\ cartella \\ idl.

Le intestazioni precompilate sono molto più semplici da usare e diversi file IDL vengono combinati in una singola intestazione fornita. Tuttavia, se si decide di elaborare i propri file di intestazione dai file IDL forniti, questo argomento descrive quali file IDL creano i file di intestazione e descrive anche le dipendenze di ogni file IDL.

**File IDL e file di intestazione forniti equivalenti**



| **Idl**                                                                                            | **Intestazione fornita equivalente**               | **Descrizione**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM.idl<br/> WMSP.idl<br/> WMSCP.idl<br/> icomponentauthenticate.idl<br/> | Mswmdm.h                                     | Tutti e quattro i file IDL sono inclusi in questa singola intestazione fornita.<br/> **WMDM.idl** definisce tutte le interfacce dell'applicazione e le strutture, le costanti e i codici di errore necessari.<br/> **WMSP.idl** definisce tutte le interfacce del provider di servizi.<br/> **WMSCP.idl** definisce tutte le interfacce, i valori GUID e le costanti richieste dai provider di contenuto sicuri.<br/> **icomponentauthenticate.idl** Definisce [**l'interfaccia IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)<br/> |
| Wmdmlog.idl                                                                                        | Wmdmlog.h<br/> wmdmlog \_ i.c<br/> | Definisce le interfacce di registrazione.<br/> Entrambi i file di intestazione forniti devono essere usati, anziché solo il file con estensione h, a causa di un problema con il file IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp.idl                                                                                 | Wmdrmdeviceapp.h                             | Definisce le [**interfacce IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usate dalle applicazioni che aggiornano DRM nei dispositivi o nei conteggi di riproduzione dei contatori nei dispositivi.                                                                                                                                                                                                                                                                                                                 |



 

**Dipendenze IDL**

Molti dei file IDL forniti hanno dipendenze di compilazione. Se si prevede di compilare i file IDL manualmente, è necessario elaborare queste dipendenze esterne nell'ordine illustrato nella tabella seguente.



|   Idl                      |   Dipendenze                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| icomponentauthenticate.idl | importare "oaidl.idl";<br/> \#include "icomponentauthenticate.idl"<br/> |
| WMDM.idl                   | Nessuna dipendenza esterna                                                         |
| WmdmLog.idl                | Nessuna dipendenza esterna                                                         |
| WMDRMDeviceApp.idl         | Nessuna dipendenza esterna                                                         |
| WMSCP.idl                  | \#includere "WMDRMDeviceApp.idl"<br/> \#includere "WMSP.idl"<br/>        |
| WMSP.idl                   | \#includere "WMDM.idl"                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni ad applicazioni e provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





