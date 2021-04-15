---
title: Interfacce di archiviazione
description: Interfacce di archiviazione
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517151"
---
# <a name="storage-interfaces"></a>Interfacce di archiviazione

I contenitori di controlli devono essere in grado di supportare i controlli che implementano [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Facoltativamente, un contenitore può supportare qualsiasi altra interfaccia di persistenza, ad esempio [**Metodo IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , per i controlli che forniscono supporto.

Una volta che un contenitore di controlli ActiveX ha scelto e inizializzato un'interfaccia di archiviazione da usare ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)e così via), l'interfaccia di archiviazione resterà l'interfaccia di archiviazione primaria per la durata del controllo, ovvero il controllo rimarrà in possesso dell'archiviazione. Questa operazione non impedisce il salvataggio del contenitore in altre interfacce di archiviazione.

I contenitori di controlli ActiveX non devono supportare un meccanismo di salvataggio come testo, quindi l'uso di [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) e l'interfaccia lato contenitore associata [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) sono facoltativi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 