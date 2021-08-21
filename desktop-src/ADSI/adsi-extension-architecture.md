---
title: Architettura dell'estensione ADSI
description: Le estensioni ADSI si basano sul modello di aggregazione COM con diversi miglioramenti. Le estensioni devono essere conformi a tutte le regole COM. Per altre informazioni, vedere la specifica COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, architettura dell'estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239a2562054f062464fc924a0f67c31ea3d9fab696fd23e532eab78e1dc66d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023871"
---
# <a name="adsi-extension-architecture"></a>Architettura dell'estensione ADSI

Le estensioni ADSI si basano sul modello di aggregazione COM con diversi miglioramenti. Le estensioni devono essere conformi a tutte le regole COM. Per altre informazioni, vedere la specifica COM.

Ecco una revisione del modello di aggregazione COM.

![modello di aggregazione com](images/comagmod.png)

Un'aggregazione, nota anche come oggetto interno, è un oggetto creato da un aggregatore. L'oggetto estensione è un'aggregazione.

Un aggregatore, noto anche come oggetto esterno, è un oggetto che crea un'aggregazione. ADSI è un aggregatore.

L'oggetto interno delega [**l'IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) all'oggetto **IUnknown dell'aggregatore.**

Le estensioni ADSI aggiungono i miglioramenti seguenti all'aggregazione COM per soddisfare i requisiti:

-   Consente a ogni writer di estensione di estendere gli oggetti ADSI. Un writer di estensioni può registrare l'estensione con ADSI e non essere interessato dall'esistenza di altre estensioni. Nel modello di aggregazione COM, l'aggregatore deve avere il CLSID dell'aggregazione. ADSI rilasce questo requisito facendosi fungere da aggregatore per tutte le estensioni. Pertanto, anziché formare un livello di componenti annidati, le estensioni sono allo stesso livello.
-   Consente un oggetto, un IDispatch. Il supporto dell'automazione è una delle funzionalità più importanti di ADSI. Il supporto per l'automazione viene ottenuto perché ADSI supporta [**l'interfaccia IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) I writer di estensioni sono invitati a supportare **l'interfaccia IDispatch.** Tuttavia, deve essere presente una sola **interfaccia IDispatch** su un determinato oggetto. ADSI integra e raccoglie le numerose interfacce **IDispatch** da estensioni diverse e le presenta come **un unico IDispatch** coerente al controller di automazione. Ogni estensione, se aggregata, deve eseguire nuovamente il routing delle chiamate **IDispatch** **all'interfaccia IDispatch** fornita da ADSI.

Tutte queste soluzioni sono possibili grazie ai servizi forniti da ADSI Object Manager, che risiedono in ogni provider ADSI.

Nella figura seguente viene illustrata l'architettura del modello di estensione ADSI.

![Architettura del modello di estensione adsi](images/adsiexmo.png)

ADSI supporta due livelli di estensione:

-   Supporto dell'associazione anticipata. Questo è il primo livello di estensione. Un'estensione deve supportare la registrazione e implementare nuove interfacce. I consumer dell'estensione devono usare strumenti o host di scripting che supportano l'associazione anticipata, ad esempio Visual C++ , Visual Basic.
-   Supporto dell'associazione tardiva. Ciò si verifica quando un'estensione soddisfa tutti i requisiti di associazione anticipata e implementa un'interfaccia aggiuntiva, [**IADsExtension.**](/windows/desktop/api/Iads/nn-iads-iadsextension) Gli implementatori di estensioni possono usare qualsiasi strumento che opera come controller di automazione, ad esempio Windows Script Host, Active Server Pages o HTML con VBScript.

 

 