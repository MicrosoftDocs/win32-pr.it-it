---
title: Architettura dell'estensione ADSI
description: Le estensioni ADSI sono basate sul modello di aggregazione COM con diversi miglioramenti. Le estensioni devono essere conformi a tutte le regole COM. Per ulteriori informazioni, vedere la specifica COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, architettura dell'estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730287"
---
# <a name="adsi-extension-architecture"></a>Architettura dell'estensione ADSI

Le estensioni ADSI sono basate sul modello di aggregazione COM con diversi miglioramenti. Le estensioni devono essere conformi a tutte le regole COM. Per ulteriori informazioni, vedere la specifica COM.

Ecco una revisione del modello di aggregazione COM.

![modello di aggregazione com](images/comagmod.png)

Un'aggregazione, nota anche come oggetto interno, è un oggetto creato da un aggregatore. L'oggetto di estensione è un'aggregazione.

Un aggregatore, noto anche come oggetto esterno, è un oggetto che crea un'aggregazione. ADSI è un aggregatore.

L'oggetto interno delega la relativa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a **IUnknown** di aggregator.

Le estensioni ADSI aggiungono i miglioramenti seguenti all'aggregazione COM per soddisfare i requisiti:

-   Consente a ogni writer di estensione di estendere gli oggetti ADSI. Un writer di estensione può registrare l'estensione con ADSI e non essere interessata dall'esistenza di altre estensioni. Nel modello di aggregazione COM, l'aggregatore deve avere il CLSID dell'aggregazione. ADSI distende questo requisito facendo in modo che funga da aggregatore per tutte le estensioni. Pertanto, anziché formare un livello di componenti annidati, le estensioni sono allo stesso livello.
-   Consente un oggetto, uno IDispatch. Il supporto di automazione è una delle funzionalità più importanti di ADSI. Il supporto per l'automazione è stato effettuato perché ADSI supporta l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . I writer di estensione sono invitati a supportare l'interfaccia **IDispatch** . Tuttavia, deve essere presente una sola interfaccia **IDispatch** su un oggetto specificato. ADSI integra e raccoglie le numerose interfacce **IDispatch** da estensioni diverse e le presenta come un **IDispatch** coerente al controller di automazione. Ogni estensione, quando aggregata, deve reindirizzare le chiamate **IDispatch** alla **IDISPATCH** fornita da ADSI.

Tutte queste soluzioni sono possibili grazie ai servizi forniti da Gestione oggetti ADSI, che risiedono in ogni provider ADSI.

Nella figura seguente è illustrata l'architettura del modello di estensione ADSI.

![architettura del modello di estensione ADSI](images/adsiexmo.png)

ADSI supporta due livelli di estensione:

-   Supporto per l'associazione anticipata. Si tratta del primo livello di estensione. Un'estensione deve supportare la registrazione e implementare nuove interfacce. I consumer di estensione devono usare gli strumenti o gli host di scripting che supportano l'associazione anticipata, ad esempio Visual C++ Visual Basic.
-   Supporto per l'associazione tardiva. Ciò si verifica quando un'estensione soddisfa tutti i requisiti di associazione anticipati e implementa un'interfaccia aggiuntiva, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Gli implementatori di estensioni possono usare qualsiasi strumento che funge da controller di automazione, ad esempio Windows script host, pagine Active Server o HTML con VBScript.

 

 