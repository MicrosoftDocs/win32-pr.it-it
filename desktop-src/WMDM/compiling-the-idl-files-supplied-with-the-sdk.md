---
title: Compilazione dei file IDL forniti con l'SDK
description: Compilazione dei file IDL forniti con l'SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gestione dispositivi, file IDL
- Gestione dispositivi, file IDL
- applicazioni desktop, file IDL
- provider di servizi, file IDL
- Guida per programmatori, file IDL
- IDL (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298505"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilazione dei file IDL forniti con l'SDK

Windows Media Gestione dispositivi SDK include sia i file di intestazione che i file IDL di origine per la maggior parte di questi file di intestazione. I file di intestazione si trovano nella \\ \\ cartella Inc nel percorso di installazione di SDK. I file IDL si trovano nella \\ cartella IDL \\ .

Le intestazioni precompilate sono molto più semplici da utilizzare e molti dei file IDL vengono combinati in un'unica intestazione fornita. Tuttavia, se si decide di elaborare i file di intestazione dai file IDL forniti, in questo argomento vengono descritti i file IDL che consentono di creare i file di intestazione, oltre a descrivere le dipendenze di ogni file IDL.

**IDL equivalente e file di intestazione forniti**



| **IDL**                                                                                            | **Intestazione fornita equivalente**               | **Descrizione**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM. idl<br/> WMSP. idl<br/> WMSCP. idl<br/> IComponentAuthenticate. idl<br/> | Mswmdm. h                                     | In questa singola intestazione fornita sono inclusi tutti e quattro i file IDL.<br/> **WMDM. idl** definisce tutte le interfacce dell'applicazione e le strutture, le costanti e i codici di errore richiesti.<br/> **WMSP. idl** definisce tutte le interfacce del provider di servizi.<br/> **WMSCP. idl** definisce tutte le interfacce, i valori GUID e le costanti richiesti dai provider di contenuti protetti.<br/> **IComponentAuthenticate. idl** definisce l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .<br/> |
| Wmdmlog. idl                                                                                        | Wmdmlog. h<br/> wmdmlog \_ i. c<br/> | Definisce le interfacce di registrazione.<br/> È necessario utilizzare entrambi i file di intestazione specificati, anziché solo il file con estensione h, a causa di un problema con il file IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp. idl                                                                                 | Wmdrmdeviceapp. h                             | Definisce le interfacce [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usate dalle applicazioni che aggiornano i DRM nei dispositivi o i conteggi di riproduzione dei contatori nei dispositivi.                                                                                                                                                                                                                                                                                                                 |



 

**Dipendenze IDL**

Molti dei file IDL forniti hanno dipendenze di compilazione. Se si prevede di compilare manualmente i file IDL, è necessario elaborare le dipendenze esterne nell'ordine indicato nella tabella seguente.



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| **IDL**                    | **Dipendenze**                                                                 |
| IComponentAuthenticate. idl | Importa "OAIDL. idl";<br/> \#Includi "IComponentAuthenticate. idl"<br/> |
| WMDM. idl                   | Nessuna dipendenza esterna                                                         |
| WmdmLog. idl                | Nessuna dipendenza esterna                                                         |
| WMDRMDeviceApp. idl         | Nessuna dipendenza esterna                                                         |
| WMSCP. idl                  | \#Includi "WMDRMDeviceApp. idl"<br/> \#Includi "WMSP. idl"<br/>        |
| WMSP. idl                   | \#Includi "WMDM. idl"                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni per le applicazioni e i provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





