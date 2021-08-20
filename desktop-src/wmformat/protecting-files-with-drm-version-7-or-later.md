---
title: Protezione dei file con DRM versione 7 o successiva
description: Protezione dei file con DRM versione 7 o successiva
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows MEDIA Format SDK, file protetti
- Advanced Systems Format (ASF), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- Advanced Systems Format (ASF), file protetti
- ASF (Advanced Systems Format),file protetti
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format),WMStubDRM.lib
- WMStubDRM.lib, creazione di file protetti
- WMStubDRM.lib, file protetti
- digital rights management (DRM),WMStubDRM.lib
- DRM (digital rights management),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcec136539f9ea5d52fb5c92cf546a965202b35e25bd22010baaf98d8fde7720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846156"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protezione dei file con DRM versione 7 o successiva

Per proteggere i file Windows Media DRM versione 7 o successiva, usare il metodo [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) dell'oggetto writer per impostare gli attributi DRM. Poiché DRM versione 7 e versioni successive abilitano licenze univoche per ogni file protetto o set di file, **l'interfaccia IWMDRMWriter** include anche metodi per la creazione di chiavi. Questi metodi vengono forniti solo per praticità.

Per proteggere i file ASF con DRM versione 7 o successiva, seguire questa procedura:

1.  Collegarsi a WMStubDRM.lib e, se necessario, scollegare wmvcore.lib.
2.  Chiamare la [**funzione WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) per creare il writer DRM. Il primo argomento è riservato e deve essere impostato su **NULL.**
3.  Impostare un profilo per il writer da usare chiamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). È necessario impostare un profilo nel writer prima di impostare gli attributi DRM. DRM è supportato solo per i profili che usano i codec Windows Audio o Windows Media Video
4.  Ottenere l'interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) dell'oggetto writer.
5.  Chiamare [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e impostare [**Use Advanced \_ \_ DRM (Usa DRM avanzato)**](use-advanced-drm.md) su **TRUE.**
6.  Se è necessario generare un nuovo valore di inizializzatore di chiave, chiamare [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). Nella maggior parte dei casi, si riutilizzerà un valore di seed di chiave generato in precedenza. Questo valore deve rimanere segreto. non viene scritto nel file.
7.  Chiamare [**IWMDRMWriter::GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) per creare un ID chiave, ovvero il secondo valore usato per creare la chiave effettiva. A differenza del valore di seed della chiave, l'ID chiave è pubblico e viene scritto nel file nell'intestazione DRM in chiaro. Creare un nuovo ID chiave per ogni nuovo file creato.
8.  Chiamare **IWMDRMWriter::GenerateSigningKeyPair** se necessario per generare una chiave pubblica e privata che verrà usata per firmare l'oggetto intestazione ASF DRM avanzato. Per altre informazioni su queste chiavi, vedere [**IWMDRMWriter::GenerateSigningKeyPair.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)
9.  Se necessario, ottenere i valori per popolare l'oggetto firma digitale dell'intestazione DRM. Se nel sistema non è installata una versione funzionante di Windows Media Rights Manager, è necessario configurare l'oggetto firma digitale dell'intestazione del file ASF specificando i quattro attributi seguenti, che devono essere tutti ottenuti da Microsoft:

    -   [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)
    -   [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)
    -   [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)

    Se è installato Windows Media Rights Manager, non è necessario impostare questi attributi nell'applicazione. Il componente DRM recupererà questi attributi e li userà per firmare automaticamente l'intestazione. Se si dispone di una versione attivata di Windows Media Rights Manager in un altro computer e si desidera riutilizzare i valori degli oggetti firma digitale, è possibile trovarli nel Registro di sistema. Il certificato del server licenze viene archiviato in HKEY LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server Certs:cert1 e il certificato radice viene archiviato in \_ \_ \\ \\ \\ \\ \\ HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert2. Quando si proteggono i file con DRM versione 7, è necessario usare i valori di queste chiavi del Registro di sistema. Per la proprietà **\_ DRM LASignaturePrivKey** usare **GenerateSigningKeysEx** (tramite Windows Media Rights Manager SDK) oppure riutilizzare il valore installato da Windows Media Rights Manager in HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License \_ \\ \\ \\ \\ Server:Info \_ Cert0. Per la proprietà **\_ LASignatureCert DRM,** usare **GenerateSigningKeysEx** (tramite Windows Media Rights Manager SDK) oppure il valore installato da Windows Media Rights Manager in HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert0.

10. Chiamare [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) tutte le volte che è necessario per configurare l'oggetto writer, che imposta gli attributi di intestazione DRM necessari in base alle esigenze. Queste proprietà vengono mantenute per la durata dell'oggetto writer o fino a quando non vengono reimpostate con un nuovo valore. Non è necessario reimpostarlo per ogni nuovo file creato.

    Le proprietà seguenti sono richieste dall'oggetto writer:

    -   [**Intestazione \_ DRMSignPrivKey**](drm-headersignprivkey.md)
    -   [**DRM \_ KeySeed**](drm-keyseed.md)
    -   [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**DRM \_ KeyID**](drm-keyid.md)
    -   [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md)

    Le proprietà seguenti sono facoltative:

    -   [**DRM \_ ContentID**](drm-contentid.md)
    -   [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)

    Inoltre, è possibile specificare gli attributi del file DRM definiti dall'utente direttamente usando [**l'attributo di base \_ DRM DRMHeader.**](drm-drmheader.md) È possibile aggiungere qualsiasi attributo aggiuntivo, ad esempio "DRMHeader.RequireSAP", per comunicare informazioni aggiuntive che verranno usate dal server licenze per la creazione della licenza. Il server licenze deve essere a conoscenza di eventuali proprietà aggiuntive che si aggiungono. Non è possibile individuare proprietà sconosciute a livello di codice.

11. Scrivere il file usando i [**metodi dell'interfaccia IWMWriter,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) come descritto altrove in questa documentazione. Per creare un flusso DRM live, è sufficiente scrivere in un sink di rete. È anche possibile scrivere in un sink di push.
12. Se necessario, creare una licenza per il file usando Windows Media Rights Manager. Questa attività può essere eseguita anche da un server licenze di terze parti. Per gli scenari DRM live, gli utenti finali dovranno ottenere una licenza prima dell'inizio del flusso o al primo tentativo di connessione.

**Nota** DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> <dt>

[**Interfaccia IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




