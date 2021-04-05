---
title: Gestione delle licenze
description: Gestione delle licenze
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730498"
---
# <a name="licensing"></a>Gestione delle licenze

Per incorporare correttamente i controlli con licenza, i contenitori di controlli ActiveX devono usare [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) anziché [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Diverse funzioni di supporto per la creazione e il caricamento OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chiamano in modo esplicito **IClassFactory** e non **IClassFactory2** e pertanto non possono essere usate per creare o caricare controlli ActiveX con licenza. I contenitori di controlli ActiveX devono creare e caricare i controlli ActiveX in modo esplicito tramite **IClassFactory2**.

 

 