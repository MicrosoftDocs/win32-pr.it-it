---
title: Implementazione di CSearch
description: Implementazione di CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-in di Windows Media Player, classe CSearch
- plug-in, classe CSearch
- plug-in dell'interfaccia utente, classe CSearch
- Plug-in dell'interfaccia utente, classe CSearch
- Classe CSearch
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515613"
---
# <a name="implementing-csearch"></a>Implementazione di CSearch

L'interfaccia **IWMPPluginUI** presenta diversi metodi che vengono chiamati da Windows Media Player in momenti diversi durante il ciclo di vita di un'istanza del plug-in. La procedura guidata fornisce le implementazioni di base di questi metodi, nonché il costruttore e il distruttore della classe e altri metodi di classe. Il file search. h deve essere modificato in modo che Windows Media Player possa comunicare con l'interfaccia utente, come descritto nella sezione successiva.

Affinché la classe CPluginWindow abbia accesso alla variabile membro privata m \_ spCore, è necessario eseguire una dichiarazione di classe Friend all'interno della definizione della classe CSearch, come illustrato nel frammento di codice seguente:


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

[**Guida alla programmazione di plug-in dell'interfaccia utente**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




