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
# <a name="ws-management-protocol"></a>Protocollo WS-Management

Il protocollo WS-Management è stato sviluppato da un gruppo di produttori di hardware e software come standard pubblico per lo scambio remoto di dati di gestione con ogni dispositivo in cui il protocollo è implementato.

## <a name="standards"></a>Standard

Per ulteriori informazioni sul protocollo WS-Management, vedere [la specifica relativa a Web Services for Management (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

Lo scopo del protocollo è fornire coerenza e interoperabilità per le operazioni di gestione in molti tipi di dispositivi (incluso il firmware) e sistemi operativi. Il protocollo WS-Management può essere esteso in quanto le nuove operazioni vengono identificate dal settore IT.

L'implementazione corrente del protocollo WS-Management si basa sulle specifiche standard seguenti: HTTPS, SOAP su HTTP (profilo WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Per ulteriori informazioni sugli standard WS-Management e XML Schema, vedere <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Messaggi

Il protocollo WS-Management fornisce uno standard per la creazione di [*messaggi*](windows-remote-management-glossary.md) XML utilizzando vari standard di servizi Web, ad esempio [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer*](windows-remote-management-glossary.md). Questi standard definiscono gli schemi XML per i messaggi del servizio Web. I messaggi fanno riferimento a una [*risorsa*](windows-remote-management-glossary.md) che usa un [*URI di risorsa*](windows-remote-management-glossary.md). Il protocollo WS-Management aggiunge un set di definizioni per le operazioni di gestione e i valori. Ad esempio, WS-Transfer definisce le operazioni get, put, create ed Delete per una risorsa. WS-Management protocollo aggiunge Rinomina, Get parziale e put parziale.

I messaggi seguono le convenzioni di [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) utilizzate da tutti i protocolli del servizio Web.

Nell'esempio di codice seguente viene illustrato un messaggio con un'operazione get. Questo esempio viene illustrato come supporto per comprendere l'aspetto dei messaggi sottostanti. Non è necessario saper produrre messaggi SOAP. I messaggi vengono assemblati da Gestione remota Windows quando si esegue un comando utilizzando lo strumento da riga di comando **WinRM** o si esegue uno script scritto con l' [API di scripting WinRM](winrm-scripting-api.md).

Il messaggio è una richiesta di ottenere l'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con una proprietà **DeviceID** "c:" da un server denominato ComputerRemoto. La richiesta usa il trasporto HTTP tramite la porta 80. L'account che invia la richiesta deve essere nel gruppo Administrators locale nel computer remoto.

I caratteri prima dei due punti all'inizio di ogni tag indicano quale standard definisce l'elemento XML. Ad esempio, ` <wsa:To>` indica che l'elemento to viene definito dal WS-Addressing standard e `<s:Header>` indica l'inizio del contenuto dell'intestazione in un messaggio SOAP. Tenere presente che la maggior parte del messaggio è costituito da elementi XML definiti da SOAP o WS-Addressing. WS-Management protocollo aggiunge MaxEnvelopeSize, Selector e SelectorSet.


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

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Gestione hardware remota](remote-hardware-management.md)
</dt> </dl>

 

 