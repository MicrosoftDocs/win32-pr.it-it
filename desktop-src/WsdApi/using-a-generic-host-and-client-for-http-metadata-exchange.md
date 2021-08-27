---
description: Se il client e l'host non possono scambiare metadati, è possibile sostituire host e client generici con l'host personalizzato e il client per risolvere il problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Uso di un host generico e di un client per i metadati HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10040f4834df1a77115a361d23d82ec3dfcc6c57
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883179"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Uso di un host generico e di un client per i metadati HTTP Exchange

Se il client e l'host non possono scambiare metadati, è possibile sostituire host e client generici con l'host personalizzato e il client per risolvere il problema. Se l'indirizzo del dispositivo o i metadati del dispositivo non vengono visualizzati nell'output del client di debug WSD, gli indirizzi di trasporto forniti o l'ambiente di rete potrebbero causare l'errore. Per altre informazioni sull'host generico e sul client, vedere [Strumenti di debug](debugging-tools.md).

Se è stato verificato che un host e un client generico possono completare lo scambio di metadati WS-Discovery e HTTP, questa procedura di diagnostica può essere ignorata e la risoluzione dei problemi può essere continuata seguendo le procedure descritte in Uso della registrazione [WinHTTP](using-winhttp-logging-to-verify-get-traffic.md)per verificare il traffico.

Se l'host o il client è un'applicazione in esecuzione in un PC, l'host o il client generico deve essere eseguito nello stesso contesto di sicurezza dell'host o del client effettivo. Ad esempio, se l'host o il client effettivo viene eseguito come amministratore, l'host o il client generico deve essere eseguito come amministratore. Inoltre, se l'host o il client è un dispositivo autonomo, deve essere completamente sostituito da un PC che esegue un host generico o un client in un contesto di sicurezza che garantisce l'accesso illimitato alla rete (ad esempio, in esecuzione come amministratore).

**Per usare un host e un client generici per risolvere i problemi di scambio di metadati HTTP**

1.  Aprire una finestra del prompt dei comandi.
2.  Eseguire il comando seguente: **WSDDebug \_host.exe /mode metadata /start**

    > [!Note]  
    > Potrebbe **Sicurezza di Windows finestra di dialogo** Avviso. In tal caso, fare **clic su Sblocca** per consentire l'esecuzione dell'host di debug WSD.

     

    Questo comando genera un output simile al seguente. Prendere nota dell'ID dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Eseguire il comando seguente: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *&lt; id &gt;*. Sostituire *&lt; ID &gt;* con l'ID dispositivo identificato nel passaggio 2.
    > [!Note]  
    > Potrebbe **Sicurezza di Windows finestra di dialogo** Avviso. In tal caso, fare **clic su Sblocca** per consentire l'esecuzione del client di debug WSD.

     

Il client di debug WSD genera un output simile al seguente.

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

Il client di debug WSD può generare molto output in una rete con molti dispositivi DPWS. L'output può essere reindirizzato a un file per semplificare l'analisi. Digitare **log tee** *&lt; &gt; filename* al prompt del client di debug WSD per reindirizzare l'output a un file. Il reindirizzamento dell'output può essere arrestato digitando **log tee stop** al prompt del client di debug WSD.

Prendere nota dell'indirizzo di riferimento dell'endpoint. Questo indirizzo EPR deve corrispondere all'ID dispositivo identificato nel passaggio 2 precedente. Verificare inoltre che il client di debug WSD stampi completamente i metadati per il dispositivo. I metadati del dispositivo `Metadata for host` iniziano con e terminano con `End of metadata` .

Se l'ID dispositivo e i metadati del dispositivo vengono visualizzati correttamente nell'output del client di debug WSD, l'errore dell'applicazione probabilmente non è correlato agli indirizzi di trasporto forniti, al sistema operativo o all'ambiente di rete. Sostituire l'host generico e il client con l'host e il client personalizzati e continuare la risoluzione dei problemi seguendo le procedure descritte in [Uso della registrazione WinHTTP per verificare il traffico.](using-winhttp-logging-to-verify-get-traffic.md)

Se l'indirizzo del dispositivo e i metadati del dispositivo non vengono visualizzati nell'output del client di debug WSD, l'errore potrebbe avere una o più delle cause seguenti:

-   L'indirizzo di trasporto annunciato dall'host non è corretto o non è valido. Il client di debug WSD tenta di ottenere i metadati del dispositivo dall'URL fornito nell'elemento **XAddrs** di [un messaggio ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md) L'URL usato per lo scambio di metadati viene visualizzato nell'output del client di debug WSD, preceduto dalla frase `Using xAddr` . L'esempio seguente mostra gli XAddrs usati per lo scambio di metadati nell'output del client di debug WSD precedente.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Se gli XAddrs forniti non sono conformi alle regole di convalida [XAddr,](xaddr-validation-rules.md)il client di debug WSD non può ottenere i metadati del dispositivo.

-   L'applicazione è in esecuzione nel contesto di sicurezza errato. Verificare che l'applicazione utilizzi le credenziali corrette e che il client e l'host dispongano di autorizzazioni sufficienti per accedere alla rete.
-   La configurazione del firewall non è valida. Seguire le istruzioni in [Inspecting Adapter and Firewall Impostazioni](inspecting-adapter-and-firewall-settings.md) per verificare che le impostazioni del firewall Windows siano corrette e che non siano presenti altre regole che rilasciano i pacchetti. Il client e l'host possono anche essere copiati in un computer "pristine" (uno con un'installazione del sistema operativo predefinita che non è mai stata unita a un dominio) per tentare di riprodurre l'errore.
-   Un criterio IPSec blocca l'applicazione. Copiare il client e l'host in un computer non soggetto ai criteri IPSec e provare a riprodurre l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



