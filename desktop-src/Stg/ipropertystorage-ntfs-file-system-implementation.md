---
title: IPropertyStorage-implementazione del file system NTFS
description: La versione NTFS 5,0 fornisce un'implementazione dell'interfaccia IPropertyStorage per i file in un volume NTFS quando i file non sono file composti.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd STG, implementazioni, NTFS file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299990"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-implementazione del file system NTFS

La versione NTFS 5,0 fornisce un'implementazione dell'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) per i file in un volume NTFS quando i file non sono file composti.

**Per ottenere un puntatore all'implementazione di file system NTFS di IPropertySetStorage**

1.  Chiamare [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) usando l'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).
2.  Chiamare [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) usando l'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

## <a name="when-to-use"></a>Utilizzo

Utilizzare [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) per gestire le proprietà all'interno di un singolo set di proprietà. I metodi supportano la lettura, la scrittura e l'eliminazione di proprietà e i nomi di stringa facoltativi che possono essere associati a identificatori di proprietà. Un altro metodo consente di impostare gli orari associati all'archiviazione delle proprietà, mentre un altro consente l'assegnazione di un CLSID, usato per associare altro codice, ad esempio il codice dell'interfaccia utente, con la proprietà impostata. La chiamata al metodo [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione NTFS di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che consente di enumerare le proprietà nel set.

## <a name="remarks"></a>Commenti

L'implementazione NTFS fornisce essenzialmente le stesse funzionalità dell'implementazione del file composto. Per altre informazioni, vedere [IPropertyStorage-implementazione del file composto](ipropertystorage-compound-file-implementation.md).

Poiché NTFS è una file system affidabile, un set di proprietà NTFS non verrà mai lasciato in uno stato non corretto. Quando il contenuto di un [**IPROPERTYSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS viene scaricato nel file NTFS sottostante, tutti gli Stati o nessuno di essi vengono scritti nel file come operazione atomica, anche se si verifica un errore durante l'operazione, ad esempio una chiusura anomala del processo. Per ottenere un comportamento simile all'implementazione del file composto, l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) padre deve essere aperta in modalità transazionale.

Questo livello di affidabilità è possibile solo quando si accede a una proprietà NTFS impostata su un volume NTFS 5,0. È possibile accedere ai set di proprietà NTFS nelle versioni precedenti di NTFS (ad esempio, un computer in cui è in esecuzione Windows NT o Windows 2000 che accede ai set di proprietà in un file server computer che esegue Windows NT 4,0), ma non è garantito che si trovino in uno stato corretto in caso di errore imprevisto.

Sebbene l'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) non supporti la transazione, l'implementazione NTFS di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) la supporta. Ovvero è possibile specificare **STGM \_ transazionale** nel parametro *GrfMode* per i metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) di **IPropertySetStorage**. Come nell'implementazione del file composto, la modalità transazionale è possibile solo per gli archivi di proprietà non semplici (specificando **PROPSETFLAG non \_ semplice** nel parametro *grfFlags* ).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-implementazione del file system NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 