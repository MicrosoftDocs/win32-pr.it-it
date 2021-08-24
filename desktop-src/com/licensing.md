---
title: Gestione delle licenze
description: Gestione delle licenze
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567741"
---
# <a name="licensing"></a>Gestione delle licenze

Per incorporare correttamente i controlli concessi in licenza, ActiveX contenitori di controlli devono usare [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) anziché [**IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) Diverse funzioni helper di creazione e caricamento OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chiamano in modo esplicito **IClassFactory** e non **IClassFactory2** e pertanto non possono essere usate per creare o caricare controlli ActiveX licenza. ActiveX contenitori di controlli devono creare e caricare in modo esplicito ActiveX controlli usando **IClassFactory2.**

 

 