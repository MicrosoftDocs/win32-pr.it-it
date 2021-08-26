---
title: Creazione e inizializzazione di un writer DRM
description: Creazione e inizializzazione di un writer DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows MEDIA Format SDK, writer DRM
- digital rights management (DRM), creazione di writer DRM
- DRM (digital rights management), creazione di writer DRM
- digital rights management (DRM), inizializzazione di writer DRM
- DRM (digital rights management), inizializzazione di writer DRM
- API estese del client DRM, writer DRM
- API estese client, writer DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24067e082de38bc396153be918025e2608246e39185c45eaa84bfe0e5c02407
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007051"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Creazione e inizializzazione di un writer DRM

I passaggi seguenti sono necessari per inizializzare un oggetto writer ASF per l'importazione di esempi di supporti crittografati in Windows Media DRM.

1.  Seguire i passaggi da 1 a 4 di [Importazione della licenza e del materiale della chiave.](importing-license-and-key-material.md)
2.  Creare e inizializzare un oggetto writer ASF usando il materiale Windows chiave DRM multimediale appropriato. Per altre informazioni, vedere [Abilitazione del supporto DRM](enabling-drm-support.md).
3.  Impostare ognuno degli attributi seguenti chiamando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   Intestazione \_ DRMSignPrivKey
    -   DRM \_ V1LicenseAcqURL
    -   DRM \_ KeyID
    -   Licenza \_ DRMAcqURL
4.  Se una versione con licenza di Windows Media Rights Manager non è installata nel computer che esegue il software, è necessario impostare anche i quattro attributi seguenti:
    -   DRM \_ LASignatureRootCert
    -   DRM \_ LASignatureCert
    -   DRM \_ LASignatureLicSrvCert
    -   DRM \_ LASignaturePrivKey
    -   L'applicazione per i certificati di crittografia necessari può essere completata compilando il contratto di licenza [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.
5.  Creare una chiave di sessione e compilare una [**struttura WMDRM \_ IMPORT SESSION \_ \_ KEY.**](wmdrm-import-session-key.md) La chiave di sessione verrà usata per crittografare una chiave contenuto. Per un esempio, vedere [Creare un esempio di chiave di sessione](create-session-key-example.md).
6.  Creare una chiave contenuto da un vettore di inizializzazione RC4 casuale e compilare una [**struttura WMDRM \_ IMPORT CONTENT \_ \_ KEY.**](wmdrm-import-content-key.md) La chiave contenuto viene usata per crittografare gli esempi di supporti. Per un esempio, vedere [Creare un esempio di chiave contenuto](create-content-key-example.md).
7.  Crittografare la chiave simmetrica con la chiave di sessione usando la crittografia RC4.
8.  Estrarre la chiave di raccolta dei certificati del computer. Per un esempio, vedere [Ottenere l'esempio di certificato del computer](get-machine-certificate-example.md).
9.  Crittografare la chiave di sessione con la chiave pubblica estratta dal certificato.
10. Compilare una [**struttura \_ \_ \_ STRUCT INIT IMPORT DI WMDRM.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)
11. Chiamare il metodo [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) per notificare all'SDK che gli esempi in arrivo nel writer sono già protetti e devono essere inviati direttamente al client DRM di Windows Media per l'importazione.
12. Chiamare [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

I passaggi rimanenti per la creazione di un file protetto da DRM sono documentati nella Guida per programmatori di Windows Media Format SDK. Per altre informazioni, vedere [Creazione di file protetti.](creating-protected-files.md)

Il passaggio successivo consiste nell'scorrere ogni campione di supporti, crittografarlo e passarlo all'oggetto writer. Per altre informazioni, vedere Gli esempi di crittografia [e importazione di supporti](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




