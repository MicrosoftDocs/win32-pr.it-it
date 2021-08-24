---
title: File dell'estensione del servizio Web
description: In questa sezione viene descritto il file dell'estensione del servizio Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Servizi Web file estensione servizio Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b11e8e871399e1a499a6cfbb68a8e66b152d8f07f4fa5f2cda6585678af8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707231"
---
# <a name="web-service-extension-file"></a>File dell'estensione del servizio Web

In questa sezione viene descritto il file dell'estensione del servizio Web.


Il file WSX (estensione del servizio WCF) è il file di estensione per consentire all'applicazione di modificare i comportamenti locali che non influiscono sulla rappresentazione dei dati in transito. Dovrebbe essere estendibile poter aggiungere nuove funzionalità in futuro senza interrompere l'interoperabilità.

La struttura complessiva di WSX simula la struttura del file XSD o WSDL, ovvero un file XML che mantiene la stessa struttura del file di input principale. Attributi aggiuntivi nello stesso token denominato nel file principale specificano gli attributi che l'applicazione vuole controllare sul comportamento predefinito.

Non è possibile eseguire alcun'operazione qui in M3. Nella versione 1 è possibile vedere che sono supportati gli attributi seguenti:

Utilizzo Specifica del campo argomento/parametro count.

Si tratta di un attributo dell'elemento, ma applicabile solo al tipo di matrice. L'attributo IsCountOf specifica l'elemento della matrice. Il campo/parametro count non viene visualizzato in transito.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

Specifica del callback di lettura/scrittura per il tipo personalizzato

Questi attributi forzano wsutil.exe generare [**WS \_ CUSTOM \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per il tipo specificato. l'attributo readcallback personalizzato specifica la routine di callback di lettura \_ e [](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) \_ writecallback personalizzato specifica la routine di callback [**di**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) scrittura.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

È possibile avere un file WSX corrispondente per descriverne il comportamento locale:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe genera il prototipo seguente per la struttura :

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




