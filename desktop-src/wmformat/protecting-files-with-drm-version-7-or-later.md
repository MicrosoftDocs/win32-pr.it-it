---
title: Protezione dei file con DRM 7 o versione successiva
description: Protezione dei file con DRM 7 o versione successiva
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, creazione di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299513"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protezione dei file con DRM 7 o versione successiva

Per proteggere i file con Windows Media DRM versione 7 o successiva, usare il metodo [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) dell'oggetto writer per impostare gli attributi DRM. Poiché DRM versione 7 e versioni successive abilitano licenze univoche per ogni file o set di file protetto, l'interfaccia **IWMDRMWriter** dispone anche di metodi per la creazione di chiavi. Questi metodi vengono forniti solo per praticità.

Per proteggere i file ASF usando DRM versione 7 o successiva, seguire questa procedura:

1.  Eseguire il collegamento a WMStubDRM. lib e, se necessario, scollegare wmvcore. lib.
2.  Chiamare la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) per creare il writer DRM. Il primo argomento è riservato e deve essere impostato su **null**.
3.  Impostare un profilo per il writer da utilizzare chiamando [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Prima di impostare gli attributi DRM, è necessario impostare un profilo nel writer. Il DRM è supportato solo per i profili che usano i codec Windows Media Audio o Windows Media Video
4.  Ottenere l'interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) dell'oggetto writer.
5.  Chiamare [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e impostare [**Usa \_ \_ DRM avanzato**](use-advanced-drm.md) su **true**.
6.  Se è necessario generare un nuovo valore di inizializzazione chiave, chiamare [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). Nella maggior parte dei casi, si riutilizzerà un valore di inizializzazione chiave che è stato generato in precedenza. Questo valore deve rimanere segreto; non viene scritto nel file.
7.  Chiamare [**IWMDRMWriter:: GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) per creare un ID chiave, ovvero il secondo valore usato per creare la chiave effettiva. A differenza del valore di inizializzazione chiave, l'ID chiave è pubblico e viene scritto nel file nell'intestazione DRM in chiaro. Creare un nuovo ID chiave per ogni nuovo file creato.
8.  Chiamare **IWMDRMWriter:: GenerateSigningKeyPair** se necessario per generare una chiave pubblica e privata che verrà usata per firmare l'oggetto intestazione Advanced DRM ASF. Per ulteriori informazioni su queste chiavi, vedere [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Se necessario, ottenere i valori per popolare l'oggetto firma digitale dell'intestazione DRM. Se nel sistema non è installata una versione funzionante di Windows Media Rights Manager, è necessario configurare l'oggetto firma digitale dell'intestazione del file ASF specificando i quattro attributi seguenti, che devono essere tutti ottenuti da Microsoft:

    -   [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)
    -   [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)
    -   [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)
    -   [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)

    Se Windows Media Rights Manager è installato, non è necessario impostare questi attributi nell'applicazione. Il componente DRM recupererà questi attributi e li userà per firmare automaticamente l'intestazione. Se si dispone di una versione attivata di Windows Media Rights Manager in un altro computer e si desidera riutilizzare i valori degli oggetti firma digitale, è possibile trovarli nel registro di sistema. Il certificato del server licenze è archiviato in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager License Server Certificates \\ \\ : cert1 e il certificato radice è archiviato in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager License Server Certificates \\ \\ : cert2. Quando si proteggono i file con DRM versione 7, è necessario usare i valori di queste chiavi del registro di sistema. Per la **\_ Proprietà DRM LASignaturePrivKey**, utilizzare **GenerateSigningKeysEx** (tramite Windows Media Rights Manager SDK) oppure riutilizzare il valore installato da Windows Media Rights Manager in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server: info \_ Cert0. Per la proprietà **DRM \_ LASignatureCert** , utilizzare **GenerateSigningKeysEx** (tramite Windows Media Rights Manager SDK) oppure il valore installato da Windows Media Rights Manager in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ Certificates: cert0.

10. Chiamare [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) il numero di volte necessario per configurare l'oggetto writer, in modo da impostare gli attributi dell'intestazione DRM necessari, se necessario. Queste proprietà vengono mantenute per la durata dell'oggetto writer o fino a quando non vengono reimpostate con un nuovo valore. Non è necessario reimpostarli per ogni nuovo file creato.

    Per l'oggetto writer sono richieste le proprietà seguenti:

    -   [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)
    -   [**Valore di inizializzazione del valore DRM \_**](drm-keyseed.md)
    -   [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)
    -   [**\_KEYID DRM**](drm-keyid.md)
    -   [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)

    Le proprietà seguenti sono facoltative:

    -   [**\_CONTENTID DRM**](drm-contentid.md)
    -   [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)

    Inoltre, è possibile specificare direttamente gli attributi del file DRM definiti dall'utente usando l'attributo di base [**DRM \_ DRMHeader**](drm-drmheader.md) . È possibile aggiungere qualsiasi attributo aggiuntivo desiderato, ad esempio "DRMHeader. RequireSAP", ad esempio, per comunicare informazioni aggiuntive che verranno utilizzate dal server licenze per la creazione della licenza. È necessario che il server licenze sia in grado di tenere in anticipo le eventuali proprietà aggiuntive aggiunte. Non è possibile individuare proprietà sconosciute a livello di codice.

11. Scrivere il file usando i metodi dell'interfaccia [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) come descritto altrove in questa documentazione. Per creare un flusso DRM Live, è sufficiente scrivere in un sink di rete. È anche possibile scrivere in un sink di push.
12. Se necessario, creare una licenza per il file utilizzando Windows Media Rights Manager. Questa attività può essere eseguita anche da un server licenze di terze parti. Per gli scenari di DRM Live, gli utenti finali dovranno ottenere una licenza prima che il flusso venga avviato, altrimenti al momento del primo tentativo di connessione.

**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.

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

[**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




