---
title: Oggetto tipo di carattere standard
description: Oggetto tipo di carattere standard
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047398"
---
# <a name="standard-font-object"></a>Oggetto tipo di carattere standard

La proprietà del tipo di carattere di ambiente standard fornita dal contenitore e la proprietà del tipo di carattere standard fornita dal controllo forniscono entrambi un oggetto tipo di carattere standard. Ovvero, questi tipi di carattere standard forniscono un puntatore **IDispatch** a un oggetto tipo di carattere standard.

L'oggetto del tipo di carattere è un'implementazione fornita dal sistema di un set di interfacce sopra il supporto del tipo di carattere GDI sottostante. Un oggetto del tipo di carattere viene creato tramite la funzione API [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) data una struttura [**FONTDESC**](/windows/win32/api/olectl/ns-olectl-fontdesc) . L'oggetto font supporta un numero di proprietà di lettura/scrittura, nonché metodi personalizzati tramite la relativa interfaccia [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)e supporta lo stesso set di proprietà (ma non i metodi) tramite un [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)dell'interfaccia dispatch. L'interfaccia dispatch viene utilizzata per le proprietà del tipo di carattere indicate in precedenza. Le proprietà corrispondono agli attributi del tipo di carattere GDI descritti nella struttura [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) .

L'oggetto font supporta inoltre l'interfaccia in uscita [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) in modo che un client possa determinare quando le proprietà del tipo di carattere cambiano. Poiché l'oggetto font supporta almeno un'interfaccia in uscita, implementa anche [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e un punto di connessione per **IPropertyNotifySink** a questo scopo.

L'oggetto Font fornisce una proprietà hFont che è un handle del tipo di carattere di Windows che è conforme agli altri attributi specificati per il tipo di carattere. L'oggetto del tipo di carattere ritarda la realizzazione di questo tipo di carattere, quindi l'impostazione consecutiva di due proprietà su un tipo di carattere non comporta la realizzazione di un tipo di carattere intermedio. Inoltre, come ottimizzazione, l'oggetto tipo di carattere standard mantiene una cache di handle del tipo di carattere. Due oggetti font nello stesso processo con proprietà identiche restituiranno lo stesso handle del tipo di carattere. L'oggetto del tipo di carattere può rimuovere i tipi di carattere da questa cache al momento, introducendo considerazioni speciali per i client che usano questa proprietà hFont. Per ulteriori informazioni, vedere [**IFont:: Get \_ Hfont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) .

L'oggetto font supporta inoltre [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in modo che possa salvare e caricare se stesso da un'istanza di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Qualsiasi altro oggetto che usa un oggetto Font internamente normalmente Salva e carica il tipo di carattere come parte della gestione della persistenza dell'oggetto.

Inoltre, l'oggetto tipo di carattere supporta [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) tramite il quale fornisce un set di proprietà contenente valori tipizzati per ogni proprietà del tipo di carattere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo](control-properties.md)
</dt> </dl>

 

 