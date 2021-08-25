---
description: Restrizioni per il campo di utilizzo
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Restrizioni per il campo di utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccfb5b7c0923bdea117371a3b6af2669bf903fb3af996f754be43d5665c1ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942673"
---
# <a name="field-of-use-restrictions"></a>Restrizioni per il campo di utilizzo

> [!Note]  
> Questo argomento si applica a Windows 7 o versione successiva.

 

Una *restrizione sul campo d'uso* è un provisioning che limita l'uso di una licenza per una determinata tecnologia.

Media Foundation fornisce un meccanismo per applicare restrizioni sul campo d'uso Media Foundation trasformazioni, in particolare i codec. Questo meccanismo richiede che MFT blocchi il proprio uso da parte delle applicazioni fino a quando l'applicazione non ha eseguito un handshake con MFT. Media Foundation non definisce l'handshake, in genere comporterebbe una sorta di scambio crittografico.

### <a name="registration-and-enumeration"></a>Registrazione ed enumerazione

Se un MFT ha restrizioni sul campo d'uso, impostare il flag **MFT \_ ENUM \_ FLAG \_ FIELDOFUSE** quando si registra MFT. Questo flag si applica alle API di registrazione MFT seguenti:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Per impostazione predefinita, i MFT registrati con questo flag sono esclusi dai risultati dell'enumerazione. Per enumerare le MFT con restrizioni field-of-use, chiamare [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e specificare il flag **MFT \_ ENUM \_ FLAG \_ FIELDOFUSE** nel *parametro Flags.* La figura seguente illustra questo processo.

![diagramma che mostra mft e un'applicazione che invia dati al Registro di sistema](images/mft-fou01.gif)

La [**funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) esclude sempre eventuali MFT con restrizioni sul campo d'uso.

### <a name="unlocking-the-mft"></a>Sblocco di MFT

Per usare un MFT con restrizioni sul campo d'uso, seguire questa procedura:

1.  L'applicazione implementa [**l'interfaccia IMFFieldOfUseMFTUnlock.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)
2.  Il [**metodo IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) accetta un puntatore all'interfaccia **IUnknown** di MFT.
3.  Nel metodo [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) l'applicazione esegue l'handshake necessario, usando qualsiasi meccanismo definito da MFT. Questo passaggio non è definito dall'API Media Foundation.
4.  Se il [**metodo Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) ha esito positivo, il MFT si sblocca.

L'applicazione specifica il [**puntatore IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) impostando [l'attributo \_ MFT FIELDOFUSE \_ UNLOCK \_ Attribute.](mft-fieldofuse-unlock-attribute.md) Esistono diversi modi per impostare questo attributo, a seconda di come l'applicazione crea il decodificatore o la pipeline di codifica:



| API                   | Come sbloccare il campo d'uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lettore di origine         | Se l'applicazione usa il lettore [di](source-reader.md) origine per decodificare un file multimediale, impostare l'attributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ nei](mft-fieldofuse-unlock-attribute.md) parametri di configurazione. Vedere [Attributi del lettore di origine](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Sink Writer           | Se l'applicazione usa il writer di sink per codificare un file multimediale, impostare l'attributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ nei](mft-fieldofuse-unlock-attribute.md) parametri di configurazione. Vedere [Attributi del writer di sink](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Transcodifica rapida        | Se l'applicazione usa la funzionalità Fast Transcode per creare una topologia di codifica, impostare l'attributo [MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md) quando si chiama [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Per altre informazioni sulla funzionalità Fast Transcode, vedere [Transcode API](transcode-api.md).                                                                                                                                                                      |
| Topologia              | Se si crea direttamente una topologia, impostare l'attributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ ](mft-fieldofuse-unlock-attribute.md) come attributo nella topologia. Vedere [Attributi della topologia](topology-attributes.md).                                                                                                                                                                                                                                                                                                                                                  |
| Oggetto attivazione MFT | Se l'applicazione enumera direttamente i decodificatori o i codificatori che userà, impostare l'attributo [MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md) sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) <br/> Impostare l'attributo prima di chiamare [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare MFT. L'oggetto di attivazione chiama [**IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) quando crea l'MFT.<br/> |



 

Il diagramma seguente illustra la relazione tra gli oggetti di attivazione MFT e [**l'interfaccia IMFFieldOfUseMFTUnlock.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)

![diagramma che mostra un'applicazione, un oggetto di attivazione e un mft con frecce a un oggetto fou, che ha una freccia verso l'alto](images/mft-fou02.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 




