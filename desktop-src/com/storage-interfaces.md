---
title: Interfacce di archiviazione
description: Interfacce di archiviazione
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549266"
---
# <a name="storage-interfaces"></a>Interfacce di archiviazione

I contenitori di controlli devono essere in grado di supportare i controlli che implementano [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit.**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) Facoltativamente, un contenitore può supportare qualsiasi altra interfaccia di persistenza, ad esempio [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) per i controlli che forniscono supporto.

Dopo che un contenitore di controlli ActiveX ha scelto e inizializzato un'interfaccia di archiviazione da usare ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)e così via), tale interfaccia di archiviazione rimarrà l'interfaccia di archiviazione primaria per la durata del controllo, ovvero il controllo rimarrà in possesso dello spazio di archiviazione. Ciò non preclude il salvataggio del contenitore in altre interfacce di archiviazione.

I contenitori di controlli ActiveX non devono supportare un meccanismo di salvataggio come testo, pertanto l'uso di [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) e dell'interfaccia sul lato contenitore [**associata IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 