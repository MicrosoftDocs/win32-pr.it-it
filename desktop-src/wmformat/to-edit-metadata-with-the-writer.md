---
title: Per modificare i metadati con il writer
description: Per modificare i metadati con il writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, modifica dei metadati con il writer
- Windows Media Format SDK, modifica dei metadati
- Formato di sistemi avanzati (ASF), modifica dei metadati con il writer
- ASF (Advanced Systems Format), modifica dei metadati con il writer
- ASF (Advanced Systems Format), modifica dei metadati
- ASF (formato di sistemi avanzati), modifica dei metadati
- metadati, modifica con il writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398766"
---
# <a name="to-edit-metadata-with-the-writer"></a>Per modificare i metadati con il writer

È possibile accedere direttamente dal writer, i metadati che entreranno nell'intestazione del file. Chiamare il metodo **QueryInterface** di qualsiasi interfaccia nell'oggetto writer per ottenere un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) . Quando si dispone di un puntatore all'interfaccia appropriata, è possibile manipolare i metadati come se il file fosse stato caricato nell'oggetto editor dei metadati. Per ulteriori informazioni sulla modifica dei metadati, vedere [utilizzo dei metadati](working-with-metadata.md).

È necessario apportare tutte le modifiche ai metadati prima di chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Se si impostano i metadati per un file, si scrive il file e quindi si prepara la scrittura di un nuovo file senza rilasciare il writer, alcuni metadati impostati per il primo file rimarranno impostati e verranno inclusi nei file successivi. Quando si scrivono più file con la stessa istanza dell'oggetto writer, sono disponibili due opzioni: controllare tutti i metadati prima di scrivere ogni file oppure scrivere solo nei metadati del writer che si applicano a tutti i file che si stanno scrivendo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




