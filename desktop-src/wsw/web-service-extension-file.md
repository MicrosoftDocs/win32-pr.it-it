---
title: File estensione servizio Web
description: In questa sezione viene descritto il file dell'estensione del servizio Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Servizi Web file estensione servizio Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339707"
---
# <a name="web-service-extension-file"></a>File estensione servizio Web

In questa sezione viene descritto il file dell'estensione del servizio Web.


File WSX (estensione servizio WCF) è il file di estensione per consentire all'applicazione di modificare i comportamenti locali che non influiscono sulla rappresentazione Wire data. Dovrebbe essere estendibile che è possibile aggiungere nuove funzionalità in futuro senza interoperabilità.

La struttura complessiva di WSX simula la struttura del file XSD o WSDL, ovvero un file XML che mantiene la stessa struttura del file di input principale. Gli attributi aggiuntivi nello stesso token denominato nel file principale specificano gli attributi che l'applicazione vuole controllare sul comportamento predefinito.

In M3 non è possibile eseguire alcuna operazione. Nella versione 1, è possibile vedere che sono supportati i seguenti attributi:

Utilizzo che specifica il campo Conteggio argomenti/parametri.

Si tratta di un attributo dell'elemento, ma applicabile solo al tipo di matrice. L'attributo IsCountOf specifica l'elemento di matrice. Il campo di conteggio/parametro non viene visualizzato in transito.

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

Impostazione del callback di lettura/scrittura per il tipo personalizzato

Questi attributi forzano wsutil.exe per generare il [**\_ \_ tipo personalizzato WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per il tipo specificato. \_l'attributo ReadCallback personalizzato specifica la routine di [**callback read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) e \_ WriteCallback personalizzato specifica la routine di [**callback Write**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

È possibile avere un file WSX corrispondente per descrivere il comportamento locale:

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

WsUtil.exe genera il seguente prototipo per la struttura:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




