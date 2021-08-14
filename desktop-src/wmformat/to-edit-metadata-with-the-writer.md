---
title: Per modificare i metadati con il writer
description: Per modificare i metadati con il writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, modifica dei metadati con il writer
- Windows MEDIA Format SDK, modifica dei metadati
- Advanced Systems Format (ASF), modifica dei metadati con il writer
- ASF (Advanced Systems Format), modifica dei metadati con il writer
- Advanced Systems Format (ASF), modifica dei metadati
- ASF (Advanced Systems Format), modifica dei metadati
- metadati, modifica con il writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d09db09a2cd7dbc50130243e322085ab2113e76f71d8b6760bd602d16f29d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197072"
---
# <a name="to-edit-metadata-with-the-writer"></a>Per modificare i metadati con il writer

È possibile accedere, direttamente dal writer, ai metadati che verranno all'interno dell'intestazione del file. Chiamare il **metodo QueryInterface** di qualsiasi interfaccia nell'oggetto writer per ottenere un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) Dopo aver creato un puntatore all'interfaccia appropriata, è possibile modificare i metadati come si farebbe se il file fosse stato caricato nell'oggetto dell'editor di metadati. Per altre informazioni sulla modifica dei metadati, vedere [Uso dei metadati](working-with-metadata.md).

È necessario apportare tutte le modifiche ai metadati prima di [**chiamare IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Se si impostano i metadati per un file, si scrive il file e quindi si prepara a scrivere un nuovo file senza rilasciare il writer, alcuni metadati impostati per il primo file rimarranno impostati e verranno inclusi nei file successivi. Quando si scrivono più file con la stessa istanza dell'oggetto writer, sono disponibili due opzioni: controllare tutti i metadati prima di scrivere ogni file o scrivere solo nei metadati del writer che si applicano a tutti i file scritti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




