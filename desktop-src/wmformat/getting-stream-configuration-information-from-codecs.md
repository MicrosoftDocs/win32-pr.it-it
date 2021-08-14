---
title: Recupero delle informazioni di configurazione del flusso dai codec
description: Recupero delle informazioni di configurazione del flusso dai codec
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flussi,configurazioni da codec
- codec, recupero di configurazioni di flusso da
- flussi, formati di codec
- codec, formati
- streams, interfaccia IWMCodecInfo
- IWMCodecInfo,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10cd131bfd263e0e9a0616b6fa9b59b3f3b03ace30a199b8b79f8b3c3f3f09f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433867"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Recupero delle informazioni di configurazione del flusso dai codec

Per i flussi audio e video che usano i codec audio e video Windows Media, è necessario ottenere i valori per le strutture di configurazione del flusso dal codec che si vuole usare. Anche se è possibile impostare questi valori manualmente, l'uso dei codec garantisce che i valori siano accurati. È consigliabile non modificare i valori in queste strutture a meno che la documentazione non consigli in modo specifico una modifica specifica.

Le informazioni dei codec vengono fornite sotto forma di formati di codec. Ogni formato di codec è un singolo formato di flusso supportato dal codec. Per altre informazioni sui formati di flusso, vedere [Formati](formats.md).

È possibile richiedere informazioni ai codec Windows Media usando le interfacce [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) dell'oggetto di gestione profili. Per ottenere [**l'interfaccia IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) di un oggetto di gestione profili, chiamare la [**funzione WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) Chiamare **QueryInterface** in **IWMProfileManager** per ottenere **IWMCodecInfo3.**

Le sezioni seguenti descrivono come ottenere le informazioni necessarie.



| Sezione                                                                                                | Descrizione                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per enumerare tutti i codec Windows multimediali installati](to-enumerate-all-installed-windows-media-codecs.md) | Descrive come usare i metodi delle interfacce **IWMCodecInfo** e **IWMCodecInfo2** per recuperare il nome e l'indice del codec di ogni codec Windows Media installato. |
| [Per enumerare i formati di codec](to-enumerate-codec-formats.md)                                           | Viene descritto come ottenere oggetti di configurazione del flusso dai codec per l'uso nei profili.                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> </dl>

 

 




