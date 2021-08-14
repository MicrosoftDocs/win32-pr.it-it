---
title: Interazione dei componenti ADSI
description: Il componente router Active Directory popola una tabella del provider ADSI dai provider ADSI installati elencati nel Registro di sistema quando riceve la prima richiesta dall'applicazione client.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181110"
---
# <a name="adsi-component-interaction"></a>Interazione dei componenti ADSI

Il componente router Active Directory popola una tabella del provider ADSI dai provider ADSI installati elencati nel Registro di sistema quando riceve la prima richiesta dall'applicazione client. Per altre informazioni sul Registro di sistema, vedere [Installazione del componente provider di esempio](installing-the-example-provider-component.md).

Le operazioni che effettuano una richiesta da una directory per un puntatore a un'interfaccia in un oggetto Active Directory vengono eseguite tramite una funzione (**GetObject** in Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C o C++) o un metodo di interfaccia ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). Nella figura seguente l'applicazione client ADSI passa tale richiesta di associazione al componente router ADSI (1). Il componente router identifica il ProgID per il provider dalla prima parte di ADsPath e usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per trovare il CLSID corrispondente nel Registro di sistema (2) e carica il componente del provider appropriato (3).

![Interazioni tra componenti adsi nel provider di esempio](images/dscspr.png)

Nella figura precedente il componente provider crea un oggetto Active Directory che rappresenta l'elemento directory denominato. Il componente di supporto ADSI esegue **un'interfaccia QueryInterface** sull'identificatore di interfaccia richiesto. Quando viene recuperato un puntatore a tale interfaccia (4), come con tutte le implementazioni client/server COM, viene quindi passato nuovamente al client (5) e da quel momento l'applicazione client funziona direttamente con il componente provider (6).

 

 