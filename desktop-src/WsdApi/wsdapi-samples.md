---
description: Sono disponibili due esempi WSDAPI con la Windows SDK per Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Esempi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754959"
---
# <a name="wsdapi-samples"></a>Esempi di WSDAPI

Sono disponibili due esempi WSDAPI con la Windows SDK per Windows Server 2008. Il codice sorgente per gli esempi è disponibile in <Windows SDK Install Folder> \\ esempi \\ Web \\ wsdapi. Questa versione dell'SDK è disponibile nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf). Gli esempi non sono disponibili in Windows Vista SDK.

L'esempio quotation Stock (disponibile in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ stockquote) illustra un servizio con la funzionalità di messaggistica di base. L'esempio di servizio file (disponibile in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ FileService) illustra un servizio con funzionalità avanzate, ad esempio la messaggistica asincrona, gli allegati e gli eventi.

Entrambi gli esempi includono i seguenti tipi di file.

-   File WSDL contenenti le descrizioni del servizio.
-   [File di configurazione WsdCodeGen](wsdcodegen-configuration-file.md) usati per generare il codice wsdapi.
-   File di origine e intestazione C++ generati.
-   File di implementazione del servizio e del client.
-   File di progetto e di soluzione di Visual Studio.

Entrambi gli esempi implementano gli host di dispositivi ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), i proxy di dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) e i proxy del servizio ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). Nell'esempio relativo al servizio file viene inoltre illustrato l'utilizzo della messaggistica asincrona ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), degli allegati ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) e degli eventi.

I file FileServiceContract. vcproj e StockQuoteContract. vcproj inclusi negli esempi chiamano [WsdCodeGen](web-services-for-devices-code-generator.md) per generare file di origine e intestazione C++ dal file WSDL specificato nel file di configurazione WsdCodeGen. Ciò significa che se il file di configurazione WSDL o WsdCodeGen di esempio viene modificato e il progetto di esempio viene ricompilato, WsdCodeGen genera automaticamente nuovi file di intestazione e di origine che riflettono le modifiche. Questo è il metodo preferito per la compilazione di applicazioni WSDAPI. WsdCodeGen viene in genere chiamato dalla riga di comando. Aprire il \* file. vcproj pertinente per visualizzare le chiamate alla riga di comando di WsdCodeGen di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni WSD in Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



