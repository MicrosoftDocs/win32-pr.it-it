---
title: Interazione componente ADSI
description: Il componente Active Directory router popola una tabella del provider ADSI dai provider ADSI installati elencati nel registro di sistema quando riceve la prima richiesta dall'applicazione client.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730207"
---
# <a name="adsi-component-interaction"></a>Interazione componente ADSI

Il componente Active Directory router popola una tabella del provider ADSI dai provider ADSI installati elencati nel registro di sistema quando riceve la prima richiesta dall'applicazione client. Per ulteriori informazioni sul Registro di sistema, vedere [installazione del componente provider di esempio](installing-the-example-provider-component.md).

Le operazioni che effettuano una richiesta da una directory per un puntatore a un'interfaccia su un oggetto Active Directory passano attraverso una funzione (**GetObject** in Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C o C++) oppure un metodo di interfaccia ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). Nella figura seguente l'applicazione client ADSI passa una richiesta di associazione al componente del router ADSI (1). Il componente router identifica il ProgID per il provider dalla prima parte di ADsPath e utilizza [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per trovare il CLSID corrispondente nel registro di sistema (2) e carica il componente provider appropriato (3).

![interazioni dei componenti ADSI nel provider di esempio](images/dscspr.png)

Nella figura precedente il componente provider crea un oggetto Active Directory che rappresenta l'elemento directory denominata. Il componente del supporto ADSI esegue un **QueryInterface** sull'identificatore di interfaccia richiesto. Quando viene recuperato un puntatore a tale interfaccia (4), come con tutte le implementazioni client/server COM, viene quindi passato di nuovo al client (5) e da quel momento in poi l'applicazione client funziona direttamente con il componente provider (6).

 

 