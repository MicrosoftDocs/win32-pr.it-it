---
title: Protocollo WS-Management
description: Standard pubblico per lo scambio remoto di dati di gestione con qualsiasi dispositivo computer che implementi il protocollo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118415"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="fb13f-103">Protocollo WS-Management</span><span class="sxs-lookup"><span data-stu-id="fb13f-103">WS-Management Protocol</span></span>

<span data-ttu-id="fb13f-104">Il protocollo WS-Management è stato sviluppato da un gruppo di produttori di hardware e software come standard pubblico per lo scambio remoto di dati di gestione con ogni dispositivo in cui il protocollo è implementato.</span><span class="sxs-lookup"><span data-stu-id="fb13f-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="fb13f-105">Standard</span><span class="sxs-lookup"><span data-stu-id="fb13f-105">Standards</span></span>

<span data-ttu-id="fb13f-106">Per ulteriori informazioni sul protocollo WS-Management, vedere [la specifica relativa a Web Services for Management (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="fb13f-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="fb13f-107">Lo scopo del protocollo è fornire coerenza e interoperabilità per le operazioni di gestione in molti tipi di dispositivi (incluso il firmware) e sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="fb13f-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="fb13f-108">Il protocollo WS-Management può essere esteso in quanto le nuove operazioni vengono identificate dal settore IT.</span><span class="sxs-lookup"><span data-stu-id="fb13f-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="fb13f-109">L'implementazione corrente del protocollo WS-Management si basa sulle specifiche standard seguenti: HTTPS, SOAP su HTTP (profilo WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="fb13f-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="fb13f-110">Per ulteriori informazioni sugli standard WS-Management e XML Schema, vedere <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="fb13f-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="fb13f-111">Messaggi</span><span class="sxs-lookup"><span data-stu-id="fb13f-111">Messages</span></span>

<span data-ttu-id="fb13f-112">Il protocollo WS-Management fornisce uno standard per la creazione di [*messaggi*](windows-remote-management-glossary.md) XML utilizzando vari standard di servizi Web, ad esempio [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fb13f-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fb13f-113">Questi standard definiscono gli schemi XML per i messaggi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="fb13f-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="fb13f-114">I messaggi fanno riferimento a una [*risorsa*](windows-remote-management-glossary.md) che usa un [*URI di risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fb13f-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fb13f-115">Il protocollo WS-Management aggiunge un set di definizioni per le operazioni di gestione e i valori.</span><span class="sxs-lookup"><span data-stu-id="fb13f-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="fb13f-116">Ad esempio, WS-Transfer definisce le operazioni get, put, create ed Delete per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb13f-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="fb13f-117">WS-Management protocollo aggiunge Rinomina, Get parziale e put parziale.</span><span class="sxs-lookup"><span data-stu-id="fb13f-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="fb13f-118">I messaggi seguono le convenzioni di [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) utilizzate da tutti i protocolli del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="fb13f-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="fb13f-119">Nell'esempio di codice seguente viene illustrato un messaggio con un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="fb13f-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="fb13f-120">Questo esempio viene illustrato come supporto per comprendere l'aspetto dei messaggi sottostanti.</span><span class="sxs-lookup"><span data-stu-id="fb13f-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="fb13f-121">Non è necessario saper produrre messaggi SOAP.</span><span class="sxs-lookup"><span data-stu-id="fb13f-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="fb13f-122">I messaggi vengono assemblati da Gestione remota Windows quando si esegue un comando utilizzando lo strumento da riga di comando **WinRM** o si esegue uno script scritto con l' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fb13f-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="fb13f-123">Il messaggio è una richiesta di ottenere l'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con una proprietà **DeviceID** "c:" da un server denominato ComputerRemoto.</span><span class="sxs-lookup"><span data-stu-id="fb13f-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="fb13f-124">La richiesta usa il trasporto HTTP tramite la porta 80.</span><span class="sxs-lookup"><span data-stu-id="fb13f-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="fb13f-125">L'account che invia la richiesta deve essere nel gruppo Administrators locale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="fb13f-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="fb13f-126">I caratteri prima dei due punti all'inizio di ogni tag indicano quale standard definisce l'elemento XML.</span><span class="sxs-lookup"><span data-stu-id="fb13f-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="fb13f-127">Ad esempio, ` <wsa:To>` indica che l'elemento to viene definito dal WS-Addressing standard e `<s:Header>` indica l'inizio del contenuto dell'intestazione in un messaggio SOAP.</span><span class="sxs-lookup"><span data-stu-id="fb13f-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="fb13f-128">Tenere presente che la maggior parte del messaggio è costituito da elementi XML definiti da SOAP o WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="fb13f-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="fb13f-129">WS-Management protocollo aggiunge MaxEnvelopeSize, Selector e SelectorSet.</span><span class="sxs-lookup"><span data-stu-id="fb13f-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="fb13f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb13f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb13f-131">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="fb13f-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fb13f-132">Gestione hardware remota</span><span class="sxs-lookup"><span data-stu-id="fb13f-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 