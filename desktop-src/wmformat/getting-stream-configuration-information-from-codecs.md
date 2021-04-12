---
title: Recupero delle informazioni di configurazione dei flussi dai codec
description: Recupero delle informazioni di configurazione dei flussi dai codec
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flussi, configurazioni da codec
- codec, recupero di configurazioni di flusso
- flussi, formati di codec
- codec, formati
- flussi, interfaccia IWMCodecInfo
- IWMCodecInfo, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398746"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Recupero delle informazioni di configurazione dei flussi dai codec

Per i flussi audio e video che usano i codec Windows Media Audio e video, è necessario ottenere i valori per le strutture di configurazione del flusso dal codec che si vuole usare. Sebbene sia possibile impostare questi valori manualmente, l'uso dei codec garantisce che i valori siano accurati. Non modificare i valori in queste strutture, a meno che nella documentazione non venga consigliata una modifica specifica.

Le informazioni dei codec sono costituite da formati di codec. Ogni formato di codec è un formato di flusso singolo supportato dal codec. Per ulteriori informazioni sui formati di flusso, vedere [formati](formats.md).

È possibile richiedere informazioni dai codec Windows Media usando le interfacce [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) dell'oggetto Profile Manager. Per ottenere l'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) di un oggetto di gestione profilo, chiamare la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Chiamare **QueryInterface** su **IWMProfileManager** per ottenere **IWMCodecInfo3**.

Le sezioni seguenti descrivono come ottenere le informazioni necessarie.



| Sezione                                                                                                | Descrizione                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per enumerare tutti i codec Windows Media installati](to-enumerate-all-installed-windows-media-codecs.md) | Viene descritto come utilizzare i metodi delle interfacce **IWMCodecInfo** e **IWMCodecInfo2** per recuperare il nome e l'indice di codec di ciascun codec Windows Media installato. |
| [Per enumerare i formati di codec](to-enumerate-codec-formats.md)                                           | Viene descritto come ottenere oggetti di configurazione del flusso dai codec da usare nei profili.                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




