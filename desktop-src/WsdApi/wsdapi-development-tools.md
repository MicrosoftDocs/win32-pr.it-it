---
description: Gli strumenti di sviluppo WSDAPI inclusi in Windows SDK (WSD CodeGen, WSD Debug Host e WSD Debug Client) consentono agli sviluppatori di creare client e dispositivi basati su WSDAPI ed eseguirne il debug.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Strumenti di sviluppo WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdad2d87ffafc337c98743f67ae022eb4d1d11616ac42940157a5785066645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130583"
---
# <a name="wsdapi-development-tools"></a>Strumenti di sviluppo WSDAPI

Gli strumenti di sviluppo WSDAPI inclusi in Windows SDK (WSD CodeGen, WSD Debug Host e WSD Debug Client) consentono agli sviluppatori di creare client e dispositivi basati su WSDAPI ed eseguirne il debug. Il codice sorgente per questi strumenti non è disponibile. Gli strumenti SDK si trovano nella directory seguente: <Windows SDK Install Folder> \\ Bin.

WSD CodeGen (wsdcodegen.exe) converte un contratto WSDL in codice C++ generato, in cui gli sviluppatori possono chiamare direttamente. Gestisce la serializzazione dei dati e la rappresentazione in transito in modo che gli sviluppatori possano concentrarsi sulla progettazione di applicazioni. Per altre informazioni su WSD CodeGen, vedere [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md). Questo strumento è disponibile in Microsoft Windows Software Development Kit (SDK) e in Windows Driver Kit (WDK).

Gli strumenti WSD Debug Host (wsddebughost.exe) e \_ WSD Debug Client (wsddebugclient.exe) consentono agli sviluppatori di eseguire il debug di client e \_ host. Questi strumenti possono essere usati per verificare ed esaminare il traffico WS-Discovery e lo scambio di metadati. Per altre informazioni sull'host di debug WSD e sul client di debug WSD, vedere [Strumenti di debug.](debugging-tools.md) Questi strumenti sono disponibili solo in Windows SDK.

È disponibile uno strumento di sviluppo aggiuntivo, denominato [WSDAPI Basic Interoperability Tool (WSDBIT),](https://msdn.microsoft.com/library/cc264250.aspx)disponibile solo in WDK. Questo strumento viene usato per testare i metodi del servizio, MTOM (Message Transmission Optimization Mechanism), gli allegati o WS-Eventing.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni WSD in Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Generatore di codice dei servizi Web nei dispositivi](web-services-for-devices-code-generator.md)
</dt> <dt>

[WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Strumenti di debug](debugging-tools.md)
</dt> </dl>

 

 



