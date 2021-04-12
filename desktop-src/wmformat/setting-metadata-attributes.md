---
title: Impostazione degli attributi dei metadati
description: Impostazione degli attributi dei metadati
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, impostazione degli attributi dei metadati
- ASF (Advanced Systems Format), impostazione degli attributi dei metadati
- ASF (Advanced Systems Format), impostazione degli attributi dei metadati
- metadati, impostazione degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398616"
---
# <a name="setting-metadata-attributes"></a>Impostazione degli attributi dei metadati

Gli attributi dei metadati vengono impostati tramite il metodo [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .

A tutti gli attributi viene assegnata una lingua dall'elenco di lingue per il file. È possibile accedere all'elenco di lingue usando l'interfaccia [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) . Per ottenere un puntatore a un'interfaccia **IWMLanguageList** , chiamare **QueryInterface** su qualsiasi interfaccia dell'oggetto da cui è stato ottenuto [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

È possibile aggiungere attributi con qualsiasi nome. Tuttavia, l'utilizzo di nomi di attributo che non sono nomi standard supportati da Windows Media Format SDK può rendere i metadati più difficili da individuare. La maggior parte delle applicazioni per la riproduzione di contenuti multimediali verificherà i valori standard. Per ulteriori informazioni, vedere [Custom Metadata](custom-metadata.md).

Non è possibile usare il numero di flusso 0xFFFF per aggiungere un attributo a livello globale. Per gli attributi a livello di file, è necessario assegnare ogni attributo a un numero di flusso specifico o a un flusso 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




