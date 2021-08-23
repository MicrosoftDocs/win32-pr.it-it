---
title: Funzioni Windows Media Format SDK
description: Funzioni
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Media Format SDK, funzioni
- Advanced Systems Format (ASF), funzioni
- ASF (Advanced Systems Format), funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560756451ee2f5b49d26b5611b38a40a45cac7643b101fdbe8ae492386901689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708261"
---
# <a name="windows-media-format-sdk-functions"></a>Funzioni Windows Media Format SDK

L Windows Media Format SDK include funzioni per la creazione di oggetti e funzioni helper per semplificare alcune procedure.

Questo SDK supporta le funzioni seguenti per la creazione iniziale di oggetti . Se un oggetto non è elencato di seguito, è necessario crearlo usando un'interfaccia da un altro oggetto. Per altre informazioni, vedere [Oggetti](objects.md).



| Funzione                                                                             | Descrizione                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Esamina l'estensione di file nell'URL o nel nome file passato come argomento                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Esamina un protocollo di rete e lo confronta con un elenco interno di schemi supportati                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Crea un oggetto di ripristino del backup.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Esegue il wrapping dei certificati dell'utente in un oggetto .                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Crea un oggetto di registrazione del dispositivo.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Crea un oggetto transcryptor DRM.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Crea un oggetto editor di metadati.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Crea un oggetto indicizzatore.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Crea un oggetto agente di revoca delle licenze.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Crea un oggetto di gestione profili.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Crea un oggetto lettore.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Crea un oggetto che implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**Certificato WMCreateSecureChannel \_**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Crea un oggetto che implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**DES certificato \_ WMCreateSecureChannel \_**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Crea un oggetto che implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                        |
| [**WMCreateSecureChannel \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Crea un oggetto che implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Crea un oggetto lettore sincrono.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Crea un oggetto writer.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Crea un oggetto sink del file writer.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Crea un oggetto sink di rete writer.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Crea un oggetto sink di push del writer.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Verifica che un file ASF possa essere riprodotto da una copia memorizzata nella cache.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Verifica la presenza di contenuto protetto da DRM in un file.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Verifica che i dati dall'inizio di un file siano coerenti con la sezione di intestazione di un tipo di file supportato da Windows Media Format SDK. |



 

Le funzioni seguenti forniscono tasti di scelta rapida utili per l'analisi dei file.



| Funzione                                             | Descrizione                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Prova a determinare se un file è leggibile dagli oggetti di Windows Media Format SDK, in base all'estensione del nome file.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Determina se un protocollo di rete è supportato dagli oggetti di Windows Media Format SDK.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Determina se un file è disponibile per la riproduzione offline.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Verifica la presenza di contenuto protetto da DRM in un file.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Prova a determinare se un file è leggibile dagli oggetti di Windows Media Format SDK analizzando i dati all'inizio del file. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
