---
title: Rivisitazione di regole di aggregazione COM con estensioni ADSI
description: Di seguito viene riportata una breve panoramica delle regole di aggregazione COM e di estensione ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Estensioni ADSI, regole di aggregazione COM
- ADSI aggregazione COM
- Rivisitazione di regole di aggregazione COM con ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730258"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Rivisitazione di regole di aggregazione COM con estensioni ADSI

Di seguito viene riportata una breve panoramica delle regole di aggregazione COM e di estensione ADSI.

-   Il metodo **CreateInstance** restituisce un puntatore a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , come indicato di seguito, che non delega alcuna chiamata di funzione a Aggregator.

    Il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) restituisce i puntatori alle interfacce supportate ed errori per le interfacce che non supporta.

    Il metodo [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa il conteggio dei riferimenti nell'oggetto di estensione aggregato.

    Il metodo [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) decrementa il conteggio dei riferimenti nell'oggetto estensione aggregato stesso e si elimina da solo quando il conteggio dei riferimenti è 0.

-   L'oggetto estensione deve archiviare il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator, ad esempio m \_ pOuterUnknown, durante l'implementazione del metodo **CreateInstance** .
-   Tutte le interfacce supportate dall'oggetto di estensione, incluso [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), devono ereditare da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), che delega tutte le chiamate di funzione a Aggregator.
    -   [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) chiama "m \_ POuterUnknown->QueryInterface"
    -   [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) chiama "m \_ POuterUnknown->AddRef"
    -   [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) chiama "m \_ POuterUnknown->Release"

I writer di estensione possono scegliere qualsiasi implementazione interna che preferiscono purché rispettino le regole di aggregazione COM standard. Tenere presente che non è necessario che un oggetto estensione funzioni come oggetto autonomo. Le estensioni sono progettate per funzionare come aggregati. Tuttavia, un'estensione può essere scritta per funzionare sia come oggetto autonomo che come aggregato.

Oltre al supporto di aggregazione COM standard, un oggetto estensione può supportare [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per funzionalità più avanzate. Se l'associazione tardiva è supportata, l'estensione deve:

-   Funzioni delegate per [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) di nuovo all'aggregatore.
-   Implementare l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 