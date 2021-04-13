---
title: Interfaccia WSDL per soluzioni VDI personalizzate
description: Gli sviluppatori possono creare servizi Web personalizzati che gestiscono soluzioni VDI (Virtual Desktop Infrastructure).
ms.assetid: ae2dad51-be37-4311-a7c3-e99b2f41bed1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, interfaccia WSDL per l'infrastruttura VDI personalizzata
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52c51c3348f41f4cd3fad990a2cc7ef94a865173
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399159"
---
# <a name="wsdl-interface-for-custom-vdi-solutions"></a><span data-ttu-id="956a7-104">Interfaccia WSDL per soluzioni VDI personalizzate</span><span class="sxs-lookup"><span data-stu-id="956a7-104">WSDL Interface for Custom VDI Solutions</span></span>

<span data-ttu-id="956a7-105">Gli sviluppatori possono creare servizi Web personalizzati che gestiscono soluzioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="956a7-105">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

<span data-ttu-id="956a7-106">A partire da Windows Server 2008 R2, i computer client possono comunicare con i servizi Web che eseguono la gestione delle macchine virtuali usando il plug-in filtro VMMWebServerClient.dll.</span><span class="sxs-lookup"><span data-stu-id="956a7-106">Beginning with Windows Server 2008 R2, client computers can communicate with web services that perform virtual machine management by using the VMMWebServerClient.dll filter plug-in.</span></span> <span data-ttu-id="956a7-107">È possibile implementare un servizio Web personalizzato che funziona con questo plug-in di filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-107">You can implement a custom web service that works with this filter plug-in.</span></span> <span data-ttu-id="956a7-108">Per comunicare con il plug-in del filtro, il servizio Web deve implementare i metodi definiti nel seguente file WSDL (Web Services Definition Language).</span><span class="sxs-lookup"><span data-stu-id="956a7-108">To communicate with the filter plug-in, your web service must implement the methods defined in the following WSDL (Web Services Definition Language) file.</span></span>


```XML
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:wsam="https://www.w3.org/2007/05/addressing/metadata" xmlns:tns="https://Microsoft.Virtualization.RDV" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Microsoft.Virtualization.RDV" xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
  <wsdl:types>
    <xsd:schema targetNamespace="https://Microsoft.Virtualization.RDV/Imports" xmlns:xs="https://www.w3.org/2001/XMLSchema">
      <xsd:import namespace="https://Microsoft.Virtualization.RDV" />
      <xsd:import namespace="http://schemas.microsoft.com/2003/10/Serialization/" />
      <xsd:import namespace="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" />
      <xs:element name="StartVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q1="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q1:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="StartVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="StartVMResult" xmlns:q2="http://schemas.microsoft.com/2003/10/Serialization/" type="q2:guid" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="SetLocale">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="locale" nillable="true" type="xs:string" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="SetLocaleResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="SetLocaleResult" nillable="true" type="xs:string" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GetVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q3="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q3:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GetVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="GetVMResult" nillable="true" xmlns:q4="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q4:VMResult" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="PlaceVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q5="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q5:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="PlaceVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="PlaceVMResult" xmlns:q6="http://schemas.microsoft.com/2003/10/Serialization/" type="q6:guid" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="JobUpdated">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="job" nillable="true" xmlns:q7="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q7:Job" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:simpleType name="NameType">
        <xs:restriction base="xs:string">
          <xs:enumeration value="COMPUTER_NAME_FQDN" />
          <xs:enumeration value="GUID" />
          <xs:enumeration value="VM_NAME" />
        </xs:restriction>
      </xs:simpleType>
      <xs:element name="NameType" nillable="true" type="tns:NameType" />
      <xs:complexType name="VMResult">
        <xs:sequence>
          <xs:element minOccurs="0" name="DetailedErrorString" nillable="true" type="xs:string" />
          <xs:element minOccurs="0" name="ErrorID" type="tns:VMError" />
          <xs:element minOccurs="0" name="VMList" nillable="true" type="tns:ArrayOfVM" />
        </xs:sequence>
      </xs:complexType>
      <xs:element name="VMResult" nillable="true" type="tns:VMResult" />
      <xs:simpleType name="VMError">
        <xs:restriction base="xs:string">
          <xs:enumeration value="ERROR_VM_SUCCESS" />
          <xs:enumeration value="ERROR_VM_START" />
          <xs:enumeration value="ERROR_VM_PLACEMENT" />
          <xs:enumeration value="ERROR_VM_SAVE" />
          <xs:enumeration value="ERROR_VM_RESTORE" />
          <xs:enumeration value="ERROR_VM_MISSING" />
          <xs:enumeration value="ERROR_JOB_NOT_FOUND" />
          <xs:enumeration value="ERROR_VM_LOCKED" />
          <xs:enumeration value="ERROR_VM_NO_PERMISSION" />
          <xs:enumeration value="ERROR_VM_STATE" />
          <xs:enumeration value="ERROR_SERVER_CONNECTION_LOST" />
          <xs:enumeration value="ERROR_SERVER_CONNECTION_SETUP" />
        </xs:restriction>
      </xs:simpleType>
      <xs:element name="VMError" nillable="true" type="tns:VMError" />
      <xs:complexType name="ArrayOfVM">
        <xs:sequence>
          <xs:element minOccurs="0" maxOccurs="unbounded" name="VM" nillable="true" type="tns:VM" />
        </xs:sequence>
      </xs:complexType>
      <xs:element name="ArrayOfVM" nillable="true" type="tns:ArrayOfVM" />
      <xs:complexType name="VM">
        <xs:sequence>
          <xs:element minOccurs="0" name="HostFQDN" nillable="true" type="xs:string" />
          <xs:element minOccurs="0" name="HostType" type="tns:VMHostType" />
          <xs:element minOccurs="0" name="ID" type="ser:guid" />
          <xs:element minOccurs="0" name="Name" nillable="true" type="xs:string" />
          <xs:element minOccurs="0" name="Status" type="tns:VMStatus" />
        </xs:sequence>
      </xs:complexType>
      <xs:element name="VM" nillable="true" type="tns:VM" />
      <xs:simpleType name="VMHostType">
        <xs:restriction base="xs:string">
          <xs:enumeration value="VM_LIBRARY" />
          <xs:enumeration value="VM_HOST" />
        </xs:restriction>
      </xs:simpleType>
      <xs:element name="VMHostType" nillable="true" type="tns:VMHostType" />
      <xs:simpleType name="VMStatus">
        <xs:restriction base="xs:string">
          <xs:enumeration value="VM_STATUS_UNKNOWN" />
          <xs:enumeration value="VM_STATUS_MIGRATING" />
          <xs:enumeration value="VM_STATUS_RUNNING" />
          <xs:enumeration value="VM_STATUS_HIBERNATED" />
          <xs:enumeration value="VM_STATUS_PAUSED" />
          <xs:enumeration value="VM_STATUS_STOPPED" />
          <xs:enumeration value="VM_STATUS_GUEST_BOOTED" />
          <xs:enumeration value="VM_STATUS_GUEST_REBOOTED" />
          <xs:enumeration value="VM_STATUS_GUEST_READY" />
        </xs:restriction>
      </xs:simpleType>
      <xs:element name="VMStatus" nillable="true" type="tns:VMStatus" />
      <xs:complexType name="Job">
        <xs:sequence>
          <xs:element minOccurs="0" name="DetailedErrorString" nillable="true" type="xs:string" />
          <xs:element minOccurs="0" name="ErrorID" type="tns:VMError" />
          <xs:element minOccurs="0" name="ID" type="ser:guid" />
          <xs:element minOccurs="0" name="Name" nillable="true" type="xs:string" />
          <xs:element minOccurs="0" name="Progress" type="xs:double" />
          <xs:element minOccurs="0" name="Status" type="tns:JobStatus" />
          <xs:element minOccurs="0" name="Step" nillable="true" type="xs:string" />
        </xs:sequence>
      </xs:complexType>
      <xs:element name="Job" nillable="true" type="tns:Job" />
      <xs:simpleType name="JobStatus">
        <xs:restriction base="xs:string">
          <xs:enumeration value="DOES_NOT_EXISTS" />
          <xs:enumeration value="RUNNING" />
          <xs:enumeration value="FAILED" />
          <xs:enumeration value="COMPLETED" />
        </xs:restriction>
      </xs:simpleType>
      <xs:element name="JobStatus" nillable="true" type="tns:JobStatus" />
    </xsd:schema>
  </wsdl:types>
  <wsdl:message name="IRDVServer_StartVM_InputMessage">
    <wsdl:part name="parameters" element="tns:StartVM" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_StartVM_OutputMessage">
    <wsdl:part name="parameters" element="tns:StartVMResponse" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_SetLocale_InputMessage">
    <wsdl:part name="parameters" element="tns:SetLocale" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_SetLocale_OutputMessage">
    <wsdl:part name="parameters" element="tns:SetLocaleResponse" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_GetVM_InputMessage">
    <wsdl:part name="parameters" element="tns:GetVM" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_GetVM_OutputMessage">
    <wsdl:part name="parameters" element="tns:GetVMResponse" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_PlaceVM_InputMessage">
    <wsdl:part name="parameters" element="tns:PlaceVM" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_PlaceVM_OutputMessage">
    <wsdl:part name="parameters" element="tns:PlaceVMResponse" />
  </wsdl:message>
  <wsdl:message name="IRDVServer_JobUpdated_OutputCallbackMessage">
    <wsdl:part name="parameters" element="tns:JobUpdated" />
  </wsdl:message>
  <wsdl:portType msc:usingSession="true" name="IRDVServer">
    <wsdl:operation msc:isInitiating="true" msc:isTerminating="false" name="StartVM">
      <wsdl:input wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/StartVM" message="tns:IRDVServer_StartVM_InputMessage" />
      <wsdl:output wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/StartVMResponse" message="tns:IRDVServer_StartVM_OutputMessage" />
    </wsdl:operation>
    <wsdl:operation msc:isInitiating="true" msc:isTerminating="false" name="SetLocale">
      <wsdl:input wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/SetLocale" message="tns:IRDVServer_SetLocale_InputMessage" />
      <wsdl:output wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/SetLocaleResponse" message="tns:IRDVServer_SetLocale_OutputMessage" />
    </wsdl:operation>
    <wsdl:operation msc:isInitiating="true" msc:isTerminating="false" name="GetVM">
      <wsdl:input wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/GetVM" message="tns:IRDVServer_GetVM_InputMessage" />
      <wsdl:output wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/GetVMResponse" message="tns:IRDVServer_GetVM_OutputMessage" />
    </wsdl:operation>
    <wsdl:operation msc:isInitiating="true" msc:isTerminating="false" name="PlaceVM">
      <wsdl:input wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/PlaceVM" message="tns:IRDVServer_PlaceVM_InputMessage" />
      <wsdl:output wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/PlaceVMResponse" message="tns:IRDVServer_PlaceVM_OutputMessage" />
    </wsdl:operation>
    <wsdl:operation msc:isInitiating="true" msc:isTerminating="false" name="JobUpdated">
      <wsdl:output wsaw:Action="https://Microsoft.Virtualization.RDV/IRDVServer/JobUpdated" message="tns:IRDVServer_JobUpdated_OutputCallbackMessage" />
    </wsdl:operation>
  </wsdl:portType>
  <wsdl:binding name="DefaultBinding_IRDVServer" type="tns:IRDVServer">
    <soap:binding transport="https://schemas.xmlsoap.org/soap/http" />
    <wsdl:operation name="StartVM">
      <soap:operation soapAction="https://Microsoft.Virtualization.RDV/IRDVServer/StartVM" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="SetLocale">
      <soap:operation soapAction="https://Microsoft.Virtualization.RDV/IRDVServer/SetLocale" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="GetVM">
      <soap:operation soapAction="https://Microsoft.Virtualization.RDV/IRDVServer/GetVM" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="PlaceVM">
      <soap:operation soapAction="https://Microsoft.Virtualization.RDV/IRDVServer/PlaceVM" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="JobUpdated">
      <soap:operation soapAction="https://Microsoft.Virtualization.RDV/IRDVServer/JobUpdated" style="document" />
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
  </wsdl:binding>
</wsdl:definitions>
```



<span data-ttu-id="956a7-109">Questo file WSDL definisce i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="956a7-109">This WSDL file defines the following methods:</span></span>

-   [<span data-ttu-id="956a7-110">GetVM</span><span class="sxs-lookup"><span data-stu-id="956a7-110">GetVM</span></span>](#getvm)
-   [<span data-ttu-id="956a7-111">JobUpdated</span><span class="sxs-lookup"><span data-stu-id="956a7-111">JobUpdated</span></span>](#jobupdated)
-   [<span data-ttu-id="956a7-112">PlaceVM</span><span class="sxs-lookup"><span data-stu-id="956a7-112">PlaceVM</span></span>](#placevm)
-   [<span data-ttu-id="956a7-113">SetLocale</span><span class="sxs-lookup"><span data-stu-id="956a7-113">SetLocale</span></span>](#setlocale)
-   [<span data-ttu-id="956a7-114">StartVM</span><span class="sxs-lookup"><span data-stu-id="956a7-114">StartVM</span></span>](#startvm)

## <a name="getvm"></a><span data-ttu-id="956a7-115">GetVM</span><span class="sxs-lookup"><span data-stu-id="956a7-115">GetVM</span></span>

<span data-ttu-id="956a7-116">Il plug-in filtro chiama questo metodo per ottenere informazioni su una macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="956a7-116">The filter plug-in calls this method to obtain information about a specified virtual machine.</span></span> <span data-ttu-id="956a7-117">Deve restituire lo stato della macchina virtuale, il nome host, il tipo di host e il GUID.</span><span class="sxs-lookup"><span data-stu-id="956a7-117">It should return the virtual machine's state, host name, host type and GUID.</span></span>

<span data-ttu-id="956a7-118">Il plug-in del filtro passa il seguente elemento al metodo.</span><span class="sxs-lookup"><span data-stu-id="956a7-118">The filter plug-in passes the following element to the method.</span></span>


```XML
      <xs:element name="GetVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q3="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q3:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



<span data-ttu-id="956a7-119">Il servizio Web deve restituire l'elemento seguente al plug-in del filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-119">The web service must return the following element to the filter plug-in.</span></span>


```XML
      <xs:element name="GetVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="GetVMResult" nillable="true" xmlns:q4="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q4:VMResult" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



## <a name="jobupdated"></a><span data-ttu-id="956a7-120">JobUpdated</span><span class="sxs-lookup"><span data-stu-id="956a7-120">JobUpdated</span></span>

<span data-ttu-id="956a7-121">Il servizio Web chiama questo metodo per notificare al plug-in del filtro che sono state apportate modifiche a un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="956a7-121">The web service calls this method to notify the filter plug-in that changes were made to an existing job.</span></span> <span data-ttu-id="956a7-122">Quando si implementa questo metodo, restituire **S \_ OK** se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="956a7-122">When you are implementing this method, return **S\_OK** if the function succeeds.</span></span> <span data-ttu-id="956a7-123">Se ha esito negativo, restituire un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="956a7-123">If it fails, return an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="956a7-124">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values)</span><span class="sxs-lookup"><span data-stu-id="956a7-124">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values)</span></span>

<span data-ttu-id="956a7-125">Il servizio Web passa l'elemento seguente al plug-in del filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-125">The web service passes the following element to the filter plug-in.</span></span>


```XML
      <xs:element name="JobUpdated">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="job" nillable="true" xmlns:q7="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q7:Job" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



## <a name="placevm"></a><span data-ttu-id="956a7-126">PlaceVM</span><span class="sxs-lookup"><span data-stu-id="956a7-126">PlaceVM</span></span>

<span data-ttu-id="956a7-127">Il plug-in filtro chiama questo metodo per eseguire la migrazione di una macchina virtuale da una libreria a un computer host.</span><span class="sxs-lookup"><span data-stu-id="956a7-127">The filter plug-in calls this method to migrate a virtual machine from a library to a host computer.</span></span> <span data-ttu-id="956a7-128">Il metodo deve generare un processo e restituire un identificatore univoco del processo al plug-in del filtro a scopo di verifica.</span><span class="sxs-lookup"><span data-stu-id="956a7-128">The method should spawn a job and return a unique job identifier to the filter plug-in for tracking purposes.</span></span> <span data-ttu-id="956a7-129">Al termine dell'elaborazione, il servizio Web deve chiamare JobUpdated.</span><span class="sxs-lookup"><span data-stu-id="956a7-129">When processing is complete, the web service should call JobUpdated.</span></span>

<span data-ttu-id="956a7-130">Il plug-in del filtro passa il seguente elemento al metodo.</span><span class="sxs-lookup"><span data-stu-id="956a7-130">The filter plug-in passes the following element to the method.</span></span>


```XML
      <xs:element name="PlaceVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q5="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q5:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



<span data-ttu-id="956a7-131">Il servizio Web deve restituire l'elemento seguente al plug-in del filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-131">The web service must return the following element to the filter plug-in.</span></span>


```XML
      <xs:element name="PlaceVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="PlaceVMResult" xmlns:q6="http://schemas.microsoft.com/2003/10/Serialization/" type="q6:guid" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



## <a name="setlocale"></a><span data-ttu-id="956a7-132">SetLocale</span><span class="sxs-lookup"><span data-stu-id="956a7-132">SetLocale</span></span>

<span data-ttu-id="956a7-133">Il plug-in filtro chiama questo metodo per specificare le impostazioni locali da utilizzare per le stringhe di errore.</span><span class="sxs-lookup"><span data-stu-id="956a7-133">The filter plug-in calls this method to specify the locale to be used for error strings.</span></span>

<span data-ttu-id="956a7-134">Il plug-in del filtro passa il seguente elemento al metodo.</span><span class="sxs-lookup"><span data-stu-id="956a7-134">The filter plug-in passes the following element to the method.</span></span>


```XML
      <xs:element name="SetLocale">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="locale" nillable="true" type="xs:string" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



<span data-ttu-id="956a7-135">Il servizio Web deve restituire l'elemento seguente al plug-in del filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-135">The web service must return the following element to the filter plug-in.</span></span>


```XML
      <xs:element name="SetLocaleResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="SetLocaleResult" nillable="true" type="xs:string" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



## <a name="startvm"></a><span data-ttu-id="956a7-136">StartVM</span><span class="sxs-lookup"><span data-stu-id="956a7-136">StartVM</span></span>

<span data-ttu-id="956a7-137">Il plug-in filtro chiama questo metodo per avviare la macchina virtuale nel computer host corrente.</span><span class="sxs-lookup"><span data-stu-id="956a7-137">The filter plug-in calls this method to start the virtual machine on the current host computer.</span></span> <span data-ttu-id="956a7-138">Se la macchina virtuale non può essere avviata nel computer host corrente, questo metodo deve eseguire la migrazione della macchina virtuale al migliore host possibile e quindi avviarla.</span><span class="sxs-lookup"><span data-stu-id="956a7-138">If the virtual machine cannot be started on the current host computer, this method should migrate the virtual machine to the best possible host and then start it.</span></span> <span data-ttu-id="956a7-139">Il metodo deve generare un processo e restituire un identificatore univoco del processo al plug-in del filtro a scopo di verifica.</span><span class="sxs-lookup"><span data-stu-id="956a7-139">The method should spawn a job and return a unique job identifier to the filter plug-in for tracking purposes.</span></span> <span data-ttu-id="956a7-140">Al termine dell'elaborazione, il servizio Web deve chiamare JobUpdated.</span><span class="sxs-lookup"><span data-stu-id="956a7-140">When processing is complete, the web service should call JobUpdated.</span></span>

<span data-ttu-id="956a7-141">Il plug-in del filtro passa il seguente elemento al metodo.</span><span class="sxs-lookup"><span data-stu-id="956a7-141">The filter plug-in passes the following element to the method.</span></span>


```XML
      <xs:element name="StartVM">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="name" nillable="true" type="xs:string" />
            <xs:element minOccurs="0" name="type" xmlns:q1="https://schemas.datacontract.org/2004/07/Microsoft.Virtualization.RDV" type="q1:NameType" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



<span data-ttu-id="956a7-142">Il servizio Web deve restituire l'elemento seguente al plug-in del filtro.</span><span class="sxs-lookup"><span data-stu-id="956a7-142">The web service must return the following element to the filter plug-in.</span></span>


```XML
      <xs:element name="StartVMResponse">
        <xs:complexType>
          <xs:sequence>
            <xs:element minOccurs="0" name="StartVMResult" xmlns:q2="http://schemas.microsoft.com/2003/10/Serialization/" type="q2:guid" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
```



 

 