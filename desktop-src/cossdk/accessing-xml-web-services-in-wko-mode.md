---
description: È possibile accedere e utilizzare qualsiasi servizio Web XML, anche se il servizio Web XML non è stato creato utilizzando COM+ o anche Microsoft Windows, purché il servizio Web XML pubblichi una descrizione WSDL della relativa sintassi.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Accesso ai servizi Web XML in modalità WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748194"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Accesso ai servizi Web XML in modalità WKO

È possibile accedere e utilizzare qualsiasi servizio Web XML, anche se il servizio Web XML non è stato creato utilizzando COM+ o anche Microsoft Windows, purché il servizio Web XML pubblichi una descrizione WSDL della relativa sintassi. È sufficiente creare un'istanza del componente usando il moniker SOAP: WSDL = URL, dove URL è l'URL della descrizione WSDL del servizio Web XML a cui si vuole accedere. Si tratta della modalità WKO (well-known Object) per l'accesso ai servizi Web XML.

È possibile chiamare i metodi dell'oggetto senza alcuna considerazione speciale. È possibile accedere al servizio Web XML tramite una query SOAP e la risposta viene interpretata in modo trasparente.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Il seguente frammento di codice di Microsoft Visual Basic illustra l'uso di un servizio Web XML in modalità WKO.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



In questo frammento di codice, che illustra l'utilizzo di un componente di un'applicazione COM+ esposta come un servizio Web XML, nomeserver è il nome di dominio completo del server che offre il servizio Web XML. vroot è la directory radice virtuale IIS dalla quale viene esposto il servizio Web XML. e progID è il ProgID del componente che si vuole usare.

## <a name="cc"></a>C/C++

Nel frammento di codice seguente viene illustrato l'utilizzo di un servizio Web XML in modalità WKO.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



In questo frammento di codice, che illustra l'utilizzo di un componente di un'applicazione COM+ esposta come un servizio Web XML, nomeserver è il nome di dominio completo del server che offre il servizio Web XML. vroot è la directory radice virtuale IIS dalla quale viene esposto il servizio Web XML. e progID è il ProgID del componente che si vuole usare.

## <a name="remarks"></a>Commenti

Quando si accede per la prima volta a un servizio Web XML in modalità WKO, COM+ genera un client proxy e lo compila in background. Questa generazione in fase di esecuzione e la mancanza di connessioni permanenti in modalità WKO generano prestazioni significativamente ridotte rispetto alla modalità CAO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Protezione dei servizi Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



