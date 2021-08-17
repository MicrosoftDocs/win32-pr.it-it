---
title: Implementazione di CSearch
description: Implementazione di CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Windows Media Player plug-in, classe CSearch
- plug-in, classe CSearch
- plug-in dell'interfaccia utente, classe CSearch
- Plug-in dell'interfaccia utente, classe CSearch
- Classe CSearch
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f99f3e232d11075bde9905169099649a3b6e754454ac10af60b8a83493fcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748156"
---
# <a name="implementing-csearch"></a>Implementazione di CSearch

**L'interfaccia IWMPPluginUI** include diversi metodi chiamati da Windows Media Player in momenti diversi durante il ciclo di vita di un'istanza del plug-in. La procedura guidata fornisce implementazioni di base di questi metodi, nonché il costruttore e il distruttore della classe e altri metodi di classe. Il file Search.h deve essere modificato in modo Windows Media Player comunicare con l'interfaccia utente, come descritto nella sezione successiva.

Per fare in modo che la classe CPluginWindow abbia accesso alla variabile membro privata m spCore, è necessario eseguire una dichiarazione di classe Friend all'interno della definizione della classe CSearch, come illustrato nel frammento di codice \_ seguente:


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia utente di programmazione dei plug-in**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




