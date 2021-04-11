---
description: Se il client e l'host non possono vedersi reciprocamente sulla rete, un host e un client generici possono sostituire l'host e il client personalizzati per risolvere il problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Uso di un host e un client generici per UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226472"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Uso di un host e un client generici per UDP WS-Discovery

Se il client e l'host non possono vedersi reciprocamente sulla rete, un host e un client generici possono sostituire l'host e il client personalizzati per risolvere il problema. Se l'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD, è probabile che l'ambiente di rete provochi l'errore. Per ulteriori informazioni sull'host e sul client generico, vedere [strumenti di debug](debugging-tools.md).

Se l'host o il client è un'applicazione in esecuzione in un computer, l'host o il client generico deve essere eseguito nello stesso contesto di sicurezza dell'host o del client effettivo. Se, ad esempio, l'host o il client effettivo viene eseguito come amministratore, l'host o il client generico deve essere eseguito come amministratore. Inoltre, se l'host o il client è un dispositivo autonomo, deve essere completamente sostituito da un PC che esegue un host o un client generico.

**Per utilizzare un host e un client generici per risolvere i problemi relativi a WS-Discovery UDP**

1.  Aprire una finestra del prompt dei comandi.
2.  Eseguire il comando seguente: **WSDDebug \_host.exe/Mode Metadata/Start**

    > [!Note]  
    > Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** . In tal caso, fare clic su **Sblocca** per consentire l'esecuzione dell'host di debug WSD.

     

    Questo comando genera un output simile al seguente. Prendere nota dell'ID del dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Eseguire il comando seguente: **WSDDebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* . Sostituire *<id>* con l'ID dispositivo identificato nel passaggio 2.
    > [!Note]  
    > Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** . In tal caso, fare clic su **Sblocca** per consentire l'esecuzione del client di debug WSD.

     

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
```

Il client di debug WSD può generare molti output in una rete con molti dispositivi DPWS. L'output può essere reindirizzato a un file per semplificare l'analisi. Digitare **log Tee** *<filename>* al prompt del client di debug WSD per reindirizzare l'output a un file. È possibile arrestare il reindirizzamento dell'output digitando **log Tee stop** al prompt del client di debug WSD.

Prendere nota dell'indirizzo EPR (endpoint Reference). Questo indirizzo EPR deve corrispondere all'ID dispositivo identificato nel passaggio 2 precedente. In tal caso, è probabile che l'errore dell'applicazione non sia correlato al sistema operativo o all'ambiente di rete. Sostituire l'host e il client generici con l'host e il client personalizzati e continuare la risoluzione dei problemi seguendo le procedure descritte in [utilizzo del client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).

Se l'ID dispositivo non corrisponde all'indirizzo EPR, l'errore dell'applicazione è probabilmente correlato al sistema operativo o all'ambiente di rete. L'errore può avere una o più delle seguenti cause:

-   L'applicazione viene eseguita nel contesto di sicurezza errato. Verificare che l'applicazione utilizzi le credenziali corrette e che il client e l'host dispongano delle autorizzazioni sufficienti per accedere alla rete.
-   La configurazione del firewall non è corretta. Seguire le istruzioni riportate in [ispezione delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md) per verificare che le impostazioni Windows Firewall siano corrette e che non siano presenti altre regole che eliminano i pacchetti. Il client e l'host possono anche essere copiati in un computer "incontaminato" (uno con un'installazione predefinita del sistema operativo che non è mai stato aggiunto a un dominio) per tentare di riprodurre l'errore.
-   Un criterio IPSec blocca l'applicazione. Copiare il client e l'host su un computer non soggetto ai criteri IPSec e provare a riprodurre l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



