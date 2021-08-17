---
title: Protocollo WS-Management
description: Uno standard pubblico per lo scambio remoto di dati di gestione con qualsiasi dispositivo computer che implementa il protocollo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a20900e77d7d686868e00f7067b23fff644255997a14c9d4c1cbdcf3d1951d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742732"
---
# <a name="ws-management-protocol"></a>Protocollo WS-Management

Il protocollo WS-Management è stato sviluppato da un gruppo di produttori di hardware e software come standard pubblico per lo scambio remoto di dati di gestione con ogni dispositivo in cui il protocollo è implementato.

## <a name="standards"></a>Standard

Per altre informazioni sul WS-Management, vedere [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

Lo scopo del protocollo è garantire coerenza e interoperabilità per le operazioni di gestione in molti tipi di dispositivi (incluso firmware) e sistemi operativi. WS-Management protocollo può essere esteso quando le nuove operazioni vengono identificate dal settore IT.

L'implementazione corrente del protocollo WS-Management si basa sulle specifiche standard seguenti: HTTPS, SOAP su HTTP (profilo WS-I), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Per altre informazioni sugli standard WS-Management e sugli schemi XML, vedere <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Messaggi

Il WS-Management fornisce uno standard per la costruzione di messaggi [*XML*](windows-remote-management-glossary.md) utilizzando vari standard del servizio Web, ad esempio [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer.*](windows-remote-management-glossary.md) Questi standard definiscono xml schema per i messaggi del servizio Web. I messaggi fanno riferimento a una [*risorsa usando*](windows-remote-management-glossary.md) un URI [*di risorsa*](windows-remote-management-glossary.md). Il WS-Management aggiunge un set di definizioni per le operazioni e i valori di gestione. Ad esempio, WS-Transfer definisce le operazioni Get, Put, Create e Delete per una risorsa. WS-Management protocollo aggiunge Rename, Partial Get e Partial Put.

I messaggi seguono le convenzioni [*di Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) utilizzato da tutti i protocolli del servizio Web.

Nell'esempio di codice seguente viene illustrato un messaggio con un'operazione Get. Questo esempio viene illustrato come supporto per comprendere l'aspetto dei messaggi sottostanti. Non è necessario sapere come generare messaggi SOAP. I messaggi vengono assemblati da gestione remota Windows quando si esegue un comando usando lo strumento da riga di comando **Winrm** o si esegue uno script scritto con l'API di [scripting winrm](winrm-scripting-api.md).

Il messaggio è una richiesta per ottenere l'istanza di [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con una proprietà **DeviceID** "c:" da un server denominato RemoteComputer. La richiesta usa il trasporto HTTP attraverso la porta 80. L'account che invia la richiesta deve essere nel gruppo Administrators locale del computer remoto.

I caratteri prima dei due punti all'inizio di ogni tag indicano quale standard definisce l'elemento XML. Ad esempio, indica che l'elemento To è definito dallo standard WS-Addressing e indica l'inizio del contenuto dell'intestazione ` <wsa:To>` `<s:Header>` in un messaggio SOAP. Tenere presente che la maggior parte del messaggio è costituita da elementi XML definiti da SOAP o WS-Addressing. WS-Management protocollo aggiunge MaxEnvelopeSize, Selector e SelectorSet.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Gestione hardware remota](remote-hardware-management.md)
</dt> </dl>

 

 