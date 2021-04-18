---
title: Plug-in di origine
description: Plug-in di origine
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media Format SDK, plug-in di origine
- ASF (Advanced Systems Format), plug-in di origine
- ASF (Advanced Systems Format), plug-in di origine
- plug-in di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299435"
---
# <a name="source-plug-ins"></a>Plug-in di origine

Un plug-in di origine è un'opzione disponibile per gli sviluppatori che desiderano implementare il proprio sistema di archiviazione per i file di Windows Media®. Un plug-in di origine consente di eseguire questa operazione tramite l'implementazione di un'interfaccia COM denominata **IStream**, un'interfaccia standard per la fornitura di dati.

Il plug-in di origine deve essere scritto come dll e la sua presenza viene resa nota all'SDK tramite una voce del registro di sistema. In questo modo è possibile implementare un numero qualsiasi di plug-in di origine. Il plug-in di origine deve esportare la funzione [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .

Per registrare un plug-in di origine, è necessario aggiungere la seguente voce del registro di sistema:

HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ Sources

Nome = "qualsiasi nome univoco"

Valore = nome percorso della dll del plug-in di origine

Una volta registrata la dll, l'applicazione può usare il metodo **IWMReader:: Open** (con l'URL appropriato come parametro) per accedere ai dati del flusso, che possono essere archiviati in file o contenitori di dati definiti dall'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




