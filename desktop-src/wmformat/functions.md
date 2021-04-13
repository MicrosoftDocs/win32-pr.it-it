---
title: Funzioni Windows Media Format SDK
description: Funzioni
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Media Format SDK, funzioni
- ASF (Advanced Systems Format), funzioni
- ASF (Advanced Systems Format), funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cab464c3384a65776b993c2423f174debd7a89d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400082"
---
# <a name="windows-media-format-sdk-functions"></a>Funzioni Windows Media Format SDK

Windows Media Format SDK include funzioni per la creazione di oggetti e funzioni di supporto per semplificare alcune procedure.

Questo SDK supporta le funzioni seguenti per la creazione iniziale di oggetti. Se un oggetto non è elencato di seguito, è necessario crearlo utilizzando un'interfaccia di un altro oggetto. Per altre informazioni, vedere [Oggetti](objects.md).



| Funzione                                                                             | Descrizione                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Esamina l'estensione del nome file nell'URL o nel nome file che viene passato come argomento                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Esamina un protocollo di rete e lo confronta con un elenco interno di schemi supportati                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Crea un oggetto di ripristino di backup.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Esegue il wrapping dei certificati dell'utente in un oggetto.                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Crea un oggetto di registrazione del dispositivo.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Crea un oggetto transcryptor DRM.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Crea un oggetto dell'editor di metadati.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Crea un oggetto indicizzatore.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Crea un oggetto dell'agente di revoca delle licenze.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Crea un oggetto di gestione profili.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Crea un oggetto Reader.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Crea un oggetto che implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**\_Certificato WMCreateSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Crea un oggetto che implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**WMCreateSecureChannel \_ Certified \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Crea un oggetto che implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)..                                                                        |
| [**WMCreateSecureChannel \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Crea un oggetto che implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Crea un oggetto Reader sincrono.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Crea un oggetto writer.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Crea un oggetto sink di file del writer.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Crea un oggetto sink di rete del writer.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Crea un oggetto sink push writer.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Verifica che un file ASF possa essere riprodotto da una copia memorizzata nella cache.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Controlla un file per il contenuto protetto da DRM.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Verifica che i dati dall'inizio di un file siano coerenti con la sezione di intestazione di un tipo di file supportato da Windows Media Format SDK. |



 

Le funzioni seguenti forniscono collegamenti pratici per l'analisi dei file.



| Funzione                                             | Descrizione                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Tenta di determinare se un file è leggibile dagli oggetti di Windows Media Format SDK, in base all'estensione del nome di file.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Determina se un protocollo di rete è supportato dagli oggetti di Windows Media Format SDK.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Determina se un file è disponibile per la riproduzione offline.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Controlla un file per il contenuto protetto da DRM.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Tenta di determinare se un file è leggibile dagli oggetti di Windows Media Format SDK analizzando i dati all'inizio del file. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
