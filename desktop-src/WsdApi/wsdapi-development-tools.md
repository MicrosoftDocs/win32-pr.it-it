---
description: Gli strumenti di sviluppo WSDAPI inclusi nel Windows SDK (WSD CodeGen, WSD debug host e WSD debug client) consentono agli sviluppatori di creare ed eseguire il debug di client e dispositivi basati su WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Strumenti di sviluppo WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309740"
---
# <a name="wsdapi-development-tools"></a>Strumenti di sviluppo WSDAPI

Gli strumenti di sviluppo WSDAPI inclusi nel Windows SDK (WSD CodeGen, WSD debug host e WSD debug client) consentono agli sviluppatori di creare ed eseguire il debug di client e dispositivi basati su WSDAPI. Il codice sorgente per questi strumenti non è disponibile. Gli strumenti SDK si trovano nella seguente directory: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) converte un contratto WSDL in codice C++ generato, che gli sviluppatori possono chiamare direttamente in. Gestisce la serializzazione dei dati e la rappresentazione Wire, in modo che gli sviluppatori possano concentrarsi sulla progettazione di applicazioni. Per altre informazioni su WSD CodeGen, vedere [servizi Web nel generatore di codice](web-services-for-devices-code-generator.md)per i dispositivi. Questo strumento è disponibile nel Software Development Kit (SDK) di Microsoft Windows e in Windows Driver Kit (WDK).

Gli strumenti WSD debug host (wsddebug \_host.exe) e WSD debug client (wsddebug \_client.exe) consentono agli sviluppatori di eseguire il debug di client e host. Questi strumenti possono essere usati per verificare e controllare WS-Discovery e il traffico di scambio dei metadati. Per ulteriori informazioni sull'host di debug WSD e sul client di debug WSD, vedere [strumenti di debug](debugging-tools.md). Questi strumenti sono disponibili solo nel Windows SDK.

È disponibile uno strumento di sviluppo aggiuntivo, denominato [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), disponibile solo in WDK. Questo strumento viene utilizzato per il test di metodi di servizio, MTOM (Message Transmission Optimization Mechanism), allegati o WS-Eventing.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni WSD in Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Generatore di codice dei servizi Web nei dispositivi](web-services-for-devices-code-generator.md)
</dt> <dt>

[Strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Strumenti di debug](debugging-tools.md)
</dt> </dl>

 

 



