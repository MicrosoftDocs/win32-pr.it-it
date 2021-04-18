---
description: Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, provare ad accedervi in modalità oggetto attivato dal client (CAO), che evita la generazione in fase di esecuzione di un proxy e migliora le prestazioni usando connessioni permanenti.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Accesso ai servizi Web XML in modalità CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304741"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Accesso ai servizi Web XML in modalità CAO

Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, provare ad accedervi in modalità oggetto attivato dal client (CAO), che evita la generazione in fase di esecuzione di un proxy e migliora le prestazioni usando connessioni permanenti. Per accedere a un servizio Web XML in modalità CAO, [esportare](exporting-a-soap-enabled-application.md) prima di tutto l'applicazione abilitata per SOAP corrispondente dal server in modalità proxy e quindi [importare](importing-a-soap-enabled-application.md) l'applicazione nel client da cui si desidera accedere all'applicazione come servizio Web XML. È quindi possibile creare un'istanza dei componenti dell'applicazione nel client esattamente come i componenti delle applicazioni locali, ad esempio usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interfaccia utente

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Nell'Visual Basic frammento di codice seguente viene illustrato l'utilizzo di un componente di un'applicazione COM+ che è stato esposto come un servizio Web XML in modalità CAO.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

Nel frammento di codice seguente viene illustrato l'utilizzo di un componente di un'applicazione COM+ che è stato esposto come un servizio Web XML in modalità CAO.


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

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Protezione dei servizi Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
