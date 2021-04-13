---
description: Limitazioni per l'utilizzo dei campi
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Limitazioni per l'utilizzo dei campi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16f57de7642fa789a08c886a32bf906faffb72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342471"
---
# <a name="field-of-use-restrictions"></a>Limitazioni per l'utilizzo dei campi

> [!Note]  
> Questo argomento si applica a Windows 7 o versione successiva.

 

Una restrizione *del campo di utilizzo* è un provisioning che limita il modo in cui è possibile utilizzare una licenza per una determinata tecnologia.

Media Foundation fornisce un meccanismo per l'applicazione di restrizioni sul campo di utilizzo per le trasformazioni di Media Foundation (MFTs), in particolare per i codec. Questo meccanismo richiede a MFT di bloccare il proprio uso da parte delle applicazioni fino a quando l'applicazione non ha eseguito un handshake con MFT. Media Foundation non definisce l'handshake, in genere comporta una sorta di scambio crittografico.

### <a name="registration-and-enumeration"></a>Registrazione ed enumerazione

Se una MFT presenta restrizioni per il campo di utilizzo, impostare il flag di **\_ enumerazione MFT \_ flag \_ FIELDOFUSE** quando si registra il MFT. Questo flag si applica alle API di registrazione MFT seguenti:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Per impostazione predefinita, MFTs registrati con questo flag sono esclusi dai risultati dell'enumerazione. Per enumerare MFTs con restrizioni per il campo di utilizzo, chiamare [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e specificare il flag di **\_ enumerazione MFT \_ \_ FIELDOFUSE** nel parametro *Flags* . La figura seguente illustra questo processo.

![diagramma che mostra MFT e un'applicazione che invia dati al registro di sistema](images/mft-fou01.gif)

La funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) esclude sempre eventuali MFTS con restrizioni di campo per l'utilizzo.

### <a name="unlocking-the-mft"></a>Sblocco di MFT

Per usare un MFT con restrizioni per il campo di utilizzo, seguire questa procedura:

1.  L'applicazione implementa l'interfaccia [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .
2.  Il metodo [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) accetta un puntatore all'interfaccia **IUnknown** di MFT.
3.  Nel metodo [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) , l'applicazione esegue l'handshake richiesto, usando qualsiasi meccanismo definito da MFT. Questo passaggio non è definito dall'API Media Foundation.
4.  Se il metodo di [**sblocco**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) riesce, il MFT si sblocca automaticamente.

L'applicazione specifica il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) impostando l'attributo dell' [ \_ \_ \_ attributo di sblocco FIELDOFUSE di MFT](mft-fieldofuse-unlock-attribute.md) . È possibile impostare questo attributo in diversi modi, a seconda del modo in cui l'applicazione crea la pipeline di codifica o decodificatore:



| API                   | Come sbloccare il campo di utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lettore di origine         | Se l'applicazione usa il [lettore di origine](source-reader.md) per decodificare un file multimediale, impostare l'attributo di [sblocco dell' \_ \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) nei parametri di configurazione. Vedere [attributi del lettore di origine](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Writer sink           | Se l'applicazione usa il writer di sink per codificare un file multimediale, impostare l'attributo di [ \_ sblocco dell' \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) nei parametri di configurazione. Vedere [attributi di sink writer](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Transcodifica veloce        | Se l'applicazione usa la funzionalità di transcodifica rapida per creare una topologia di codifica, impostare l' [ \_ attributo di \_ sblocco \_ MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) quando si chiama [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Per ulteriori informazioni sulla funzionalità di transcodifica rapida, vedere [transcode API](transcode-api.md).                                                                                                                                                                      |
| Topologia              | Se si crea una topologia direttamente, impostare [l' \_ \_ \_ attributo di sblocco MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) come attributo nella topologia. Vedere [attributi della topologia](topology-attributes.md).                                                                                                                                                                                                                                                                                                                                                  |
| Oggetto attivazione MFT | Se l'applicazione enumera direttamente i decodificatori o i codificatori che utilizzerà, impostare l'attributo di [ \_ sblocco MFT \_ \_ FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) nei puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . <br/> Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare il MFT. L'oggetto Activation chiama [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) quando crea il MFT.<br/> |



 

Il diagramma seguente illustra la relazione tra gli oggetti di attivazione MFT e l'interfaccia [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .

![diagramma che mostra un'applicazione, un oggetto di attivazione e un MFT con frecce a un oggetto Fou, che ha una freccia verso il MFT](images/mft-fou02.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




