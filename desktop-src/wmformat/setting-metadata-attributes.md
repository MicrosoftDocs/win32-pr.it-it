---
title: Impostazione degli attributi dei metadati
description: Impostazione degli attributi dei metadati
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, impostazione degli attributi dei metadati
- Advanced Systems Format (ASF), impostazione degli attributi dei metadati
- ASF (Advanced Systems Format), impostazione degli attributi dei metadati
- metadati,impostazione di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa352a83e758b97bde6088377f8461a62b2d5071314d45f4978035bec219a5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197511"
---
# <a name="setting-metadata-attributes"></a>Impostazione degli attributi dei metadati

Gli attributi dei metadati vengono impostati usando il [**metodo IWMHeaderInfo3::AddAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)

A tutti gli attributi viene assegnata una lingua dall'elenco delle lingue per il file. È possibile accedere all'elenco di lingue usando [**l'interfaccia IWMLanguageList.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) Per ottenere un puntatore a **un'interfaccia IWMLanguageList,** chiamare **QueryInterface** su qualsiasi interfaccia dell'oggetto da cui è stato ottenuto [**IWMHeaderInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)

È possibile aggiungere attributi con qualsiasi nome. Tuttavia, l'uso di nomi di attributi che non sono nomi standard supportati da Windows Media Format SDK può rendere i metadati difficili da individuare per gli utenti. La maggior parte delle applicazioni per la riproduzione di contenuti multimediali verifica la presenza di valori standard. Per altre informazioni, vedere [Metadati personalizzati.](custom-metadata.md)

Non è possibile usare il numero di 0xFFFF per aggiungere un attributo a livello globale. È necessario assegnare ogni attributo a un numero di flusso specifico o il flusso 0 per gli attributi a livello di file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




