---
description: Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, è consigliabile accedervi in modalità CAO (Client-Activated Object), che evita la generazione in fase di esecuzione di un proxy e aumenta le prestazioni usando connessioni permanenti.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Accesso ai servizi Web XML in modalità CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549460"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Accesso ai servizi Web XML in modalità CAO

Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, è consigliabile accedervi in modalità CAO (Client-Activated Object), che evita la generazione in fase di esecuzione di un proxy e aumenta le prestazioni usando connessioni permanenti. Per accedere a un servizio Web [](exporting-a-soap-enabled-application.md) XML in modalità CAO, esportare prima [](importing-a-soap-enabled-application.md) l'applicazione abilitata per SOAP corrispondente dal server in modalità proxy e quindi importare l'applicazione nel client da cui si vuole accedere all'applicazione come servizio Web XML. È quindi possibile creare un'istanza dei componenti dell'applicazione nel client esattamente come i componenti delle applicazioni locali, ad esempio usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interfaccia utente

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Il frammento Visual Basic codice seguente illustra l'uso di un componente di un'applicazione COM+ esposto come servizio Web XML in modalità CAO.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

Il frammento di codice seguente illustra l'uso di un componente di un'applicazione COM+ esposto come servizio Web XML in modalità CAO.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Cenni preliminari sul servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Protezione dei servizi Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
