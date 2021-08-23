---
title: Archiviazione Interfacce
description: Archiviazione Interfacce
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c378b37c020f15e0fe497249b2834faffefc232bc184564f80fdb247550033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129703"
---
# <a name="storage-interfaces"></a>Archiviazione Interfacce

I contenitori di controlli devono essere in grado di supportare i controlli che implementano [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit.**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) Facoltativamente, un contenitore può supportare qualsiasi altra interfaccia di persistenza, ad esempio [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) per i controlli che forniscono supporto.

Dopo che un contenitore di controlli ActiveX ha scelto e inizializzato un'interfaccia di archiviazione da usare ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)e così via), tale interfaccia di archiviazione rimarrà l'interfaccia di archiviazione primaria per la durata del controllo, ovvero il controllo rimarrà in possesso dello spazio di archiviazione. Ciò non preclude il salvataggio del contenitore in altre interfacce di archiviazione.

ActiveX contenitori di controlli contenitori non devono supportare un meccanismo di salvataggio come testo, pertanto l'uso di [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) e dell'interfaccia sul lato contenitore [**associata IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 