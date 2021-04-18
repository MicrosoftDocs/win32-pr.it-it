---
title: Creazione e inizializzazione di un writer DRM
description: Creazione e inizializzazione di un writer DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK, writer DRM
- Digital Rights Management (DRM), creazione di writer DRM
- DRM (Digital Rights Management), creazione di writer DRM
- Digital Rights Management (DRM), inizializzazione di writer DRM
- DRM (Digital Rights Management), inizializzazione di writer DRM
- API estese del client DRM, writer DRM
- API estese client, writer DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300614"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Creazione e inizializzazione di un writer DRM

I passaggi seguenti sono necessari per inizializzare un oggetto writer ASF per l'importazione di esempi di supporti crittografati in Windows Media DRM.

1.  Eseguire i passaggi da 1 a 4 di [importazione della licenza e del materiale della chiave](importing-license-and-key-material.md).
2.  Creare e inizializzare un oggetto writer ASF utilizzando il materiale della chiave DRM di Windows Media appropriato. Per ulteriori informazioni, vedere [Abilitazione del supporto DRM](enabling-drm-support.md).
3.  Impostare ciascuno dei seguenti attributi chiamando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   \_HEADERSIGNPRIVKEY DRM
    -   \_V1LICENSEACQURL DRM
    -   \_KEYID DRM
    -   \_LICENSEACQURL DRM
4.  Se una versione con licenza di Windows Media Rights Manager non è installata nel computer in cui è in esecuzione il software, è necessario impostare anche i quattro attributi seguenti:
    -   \_LASIGNATUREROOTCERT DRM
    -   \_LASIGNATURECERT DRM
    -   \_LASIGNATURELICSRVCERT DRM
    -   \_LASIGNATUREPRIVKEY DRM
    -   Per completare l'applicazione per i certificati di crittografia necessari, compilare il [contratto di licenza di Windows Media (WMLA)](https://www.microsoft.com/licensing/default) online.
5.  Creare una chiave di sessione e compilare una struttura di [**\_ chiave della \_ sessione \_ di importazione WMDRM**](wmdrm-import-session-key.md) . La chiave della sessione verrà usata per crittografare una chiave simmetrica. Per un esempio, vedere [esempio di creazione](create-session-key-example.md)di una chiave di sessione.
6.  Creare una chiave simmetrica da un vettore di inizializzazione RC4 casuale e compilare una struttura [**WMDRM \_ import \_ Content \_ Key**](wmdrm-import-content-key.md) . La chiave simmetrica viene usata per crittografare gli esempi di contenuti multimediali. Per un esempio, vedere [creare una chiave](create-content-key-example.md)simmetrica di esempio.
7.  Crittografare la chiave simmetrica con la chiave della sessione, usando la crittografia RC4.
8.  Estrarre la chiave di raccolta del certificato del computer. Per un esempio, vedere [ottenere un certificato del computer](get-machine-certificate-example.md).
9.  Crittografare la chiave della sessione con la chiave pubblica estratta dal certificato.
10. Compilare una struttura [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .
11. Chiamare il metodo [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) per inviare una notifica all'SDK che i campioni che entrano nel writer sono già protetti e devono essere inviati direttamente al client Windows Media DRM per l'importazione.
12. Chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

I passaggi rimanenti per la creazione di un file protetto da DRM sono documentati nella Guida alla programmazione di Windows Media Format SDK. Per ulteriori informazioni, vedere [creazione di file protetti](creating-protected-files.md).

Il passaggio successivo consiste nell'eseguire l'iterazione di ogni esempio multimediale, crittografarlo e passarlo all'oggetto writer. Per ulteriori informazioni, vedere la pagina relativa alla [crittografia e all'importazione di esempi di supporti](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




