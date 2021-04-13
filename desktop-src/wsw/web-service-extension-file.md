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
# <a name="web-service-extension-file"></a><span data-ttu-id="271d8-106">File estensione servizio Web</span><span class="sxs-lookup"><span data-stu-id="271d8-106">Web Service Extension File</span></span>

<span data-ttu-id="271d8-107">In questa sezione viene descritto il file dell'estensione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="271d8-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="271d8-108">File WSX (estensione servizio WCF) è il file di estensione per consentire all'applicazione di modificare i comportamenti locali che non influiscono sulla rappresentazione Wire data.</span><span class="sxs-lookup"><span data-stu-id="271d8-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="271d8-109">Dovrebbe essere estendibile che è possibile aggiungere nuove funzionalità in futuro senza interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="271d8-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="271d8-110">La struttura complessiva di WSX simula la struttura del file XSD o WSDL, ovvero un file XML che mantiene la stessa struttura del file di input principale.</span><span class="sxs-lookup"><span data-stu-id="271d8-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="271d8-111">Gli attributi aggiuntivi nello stesso token denominato nel file principale specificano gli attributi che l'applicazione vuole controllare sul comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="271d8-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="271d8-112">In M3 non è possibile eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="271d8-112">We might not do anything here in M3.</span></span> <span data-ttu-id="271d8-113">Nella versione 1, è possibile vedere che sono supportati i seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="271d8-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="271d8-114">Utilizzo che specifica il campo Conteggio argomenti/parametri.</span><span class="sxs-lookup"><span data-stu-id="271d8-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="271d8-115">Si tratta di un attributo dell'elemento, ma applicabile solo al tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="271d8-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="271d8-116">L'attributo IsCountOf specifica l'elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="271d8-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="271d8-117">Il campo di conteggio/parametro non viene visualizzato in transito.</span><span class="sxs-lookup"><span data-stu-id="271d8-117">The count field/parameter does not appear on wire.</span></span>

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

<span data-ttu-id="271d8-118">Impostazione del callback di lettura/scrittura per il tipo personalizzato</span><span class="sxs-lookup"><span data-stu-id="271d8-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="271d8-119">Questi attributi forzano wsutil.exe per generare il [**\_ \_ tipo personalizzato WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per il tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="271d8-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="271d8-120">\_l'attributo ReadCallback personalizzato specifica la routine di [**callback read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) e \_ WriteCallback personalizzato specifica la routine di [**callback Write**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .</span><span class="sxs-lookup"><span data-stu-id="271d8-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="271d8-121">È possibile avere un file WSX corrispondente per descrivere il comportamento locale:</span><span class="sxs-lookup"><span data-stu-id="271d8-121">We can have a matching WSX file to describe its local behavior:</span></span>

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

<span data-ttu-id="271d8-122">WsUtil.exe genera il seguente prototipo per la struttura:</span><span class="sxs-lookup"><span data-stu-id="271d8-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




